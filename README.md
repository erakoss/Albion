# Albion
Albion programs, like profitability of food crafting

#Program podliczajacy koszt wytworzenia danego dania, cena za dany produkt moze byc zmieniana
#w tak aby uwzgendic czy skladnik jest nasz czy zakupiony na auckcji

# Podstawowe info o jedzeniu:
# Soup: zwieksza regeneracje hp o 100-300% na godzine;
# Salad: zwieksza szybkosc i jakosc craftingu o 33-100% na 5 min;
# Meat Pie: zwieksza szybkosc zbierania o 33-100% i pojemnosc plecaka o 10-30%;
# Omelette: zwieksza casting speed i redukuje CD o 5-85% na godzine;
# Stew: zwieksz dmg o 5-15% na godzine.

#Func stew price


def goat_stew_t4(g_meat, bread, turnip):
    price = (8*g_meat + 4*bread +4*turnip)/10
    print("Price for one stew: " + str(price))


def goat_stew_t6(g_meat, bread, turnip):
    price = (24*g_meat + 12*bread +12*turnip)/10
    print("Price for one stew: " + str(price))


def goat_stew_t8(g_meat, bread, turnip):
    price = (72*g_meat + 36*bread +36*turnip)/10
    print("Price for one stew: " + str(price))

#Func omle price


def chicken_oml_t3(raw_chick , wheat , egg_chick):
    price = ((8*raw_chick + 4*wheat + 2*egg_chick)/10)
    print("Price for one omlet: " + str(price))


def chicken_oml_t5(raw_chick , wheat , egg_chick):
    price = ((24*raw_chick + 12*wheat + 6*egg_chick)/10)
    print("Price for one omlet: " + str(price))


def chicken_oml_t7(raw_chick , wheat , egg_chick):
    price = ((72*raw_chick + 36*wheat + 18*egg_chick)/10)
    print("Price for one omlet: " + str(price))

# Func Pie price


def pie_t3(raw, flour, wheat):
    price = ((8*raw + 4*flour + 2*wheat)/10)
    print("Price for one pie: " + str(price))


def pie_t5(raw, flour, wheat, wegg):
    price = ((24*raw + 12*flour + 6*wheat + 6*wegg)/10)
    print("Price for one pie: " + str(price))


def pie_t7(raw, flour, wheat, wegg):
    price = ((72*raw + 36*flour + 18*wheat + 18*wegg)/10)
    print("Price for one pie: " + str(price))

# Func Sandwich price


def sandwich_t4(raw, flour, wheat):
    price = ((8*raw + 4*flour + 2*wheat)/10)
    print("Price for one sandwich: " + str(price))


def sandwich_t6(raw, flour, wheat):
    price = ((24*raw + 12*flour + 6*wheat)/10)
    print("Price for one sandwich: " + str(price))


def sandwich_t8(raw, flour, wheat):
    price = ((72*raw + 36*flour + 18*wheat)/10)
    print("Price for one sandwich: " + str(price))


while True:
    print("Options")
    print("Enter 'soup' to choose soup menu")
    print("Enter 'omlet' to choose omelette menu")
    print("Enter 'salad' to choose salad menu")
    print("Enter 'pie' to choose pie menu")
    print("Enter 'sandwich' to choose sandwich menu")
    print("Enter 'stew' to choose stew menu")
    print("Enter 'quit' to quit program")

    user_input = input(": ")

    if user_input == 'quit':
        break

    elif len(user_input) <= 0 or not user_input.isalpha():
        print("Use only defined word!")

    elif user_input == 'soup':
        user_input2 = input("Choose soup tier (1, 3, 5): ")

        if user_input2 == '1':
            ing1 = float(input("Carrot price? "))
            result = (16 * ing1 / 10)
            print("Price for one: " + str(result))

        elif user_input2 == '3':
            ing1 = float(input("Wheat price? "))
            result = (48 * ing1 / 10)
            print("Price for one: " + str(result))

        elif user_input2 == '5':
            ing1 = float(input("Cabbege price? "))
            result = (144 * ing1 / 10)
            print("Price for one: " + str(result))

        else:
            print("Try again")

    elif user_input == 'stew':
        user_input2 = input("Choose stew tier (4, 6, 8): ")

        if user_input2 == '4':
            ing1 = int(input("Raw goat meat price? "))
            ing2 = int(input("Bread price? "))
            ing3 = int(input("Turnip price? "))
            goat_stew_t4(ing1, ing2, ing3)

        elif user_input2 == '6':
            ing1 = int(input("Raw mutton meat price? "))
            ing2 = int(input("Bread price? "))
            ing3 = int(input("Potato price? "))
            goat_stew_t6(ing1, ing2, ing3)

        elif user_input2 == '8':
            ing1 = int(input("Raw beef meat price? "))
            ing2 = int(input("Bread price? "))
            ing3 = int(input("Pumpkin price? "))
            goat_stew_t8(ing1, ing2, ing3)

        else:
            print("Try again")

    elif user_input == 'omlet':
        user_input2 = input("Choose omlet tier (3, 5, 7): ")

        if user_input2 == '3':
            ing1 = int(input("Raw chicken meat price? "))
            ing2 = int(input("Wheat price? "))
            ing3 = int(input("Chicken egg price? "))
            chicken_oml_t3(ing1, ing2, ing3)

        elif user_input2 == '5':
            ing1 = int(input("Raw goose meat price? "))
            ing2 = int(input("Goose egg price? "))
            ing3 = int(input("Cabbage price? "))
            chicken_oml_t5(ing1, ing2, ing3)

        elif user_input2 == '7':
            ing1 = int(input("Raw pork meat price? "))
            ing2 = int(input("Bread price? "))
            ing3 = int(input("Pumpkin price? "))
            chicken_oml_t7(ing1, ing2, ing3)

        else:
            print("Try again")

    elif user_input == 'salad':
        user_input2 = input("Choose salad tier (2, 4, 6): ")

        if user_input2 == '2':
            ing1 = float(input("Bean price? "))
            ing2 = float(input("Carrot price? "))
            result = ((16 * ing1 + 16 * ing2) / 10)
            print("Price for one: " + str(result))

        elif user_input2 == '4':
            ing1 = float(input("Turnip price? "))
            ing2 = float(input("Wheat price? "))
            result = ((24 * ing1 + 24 * ing2) / 10)
            print("Price for one: " + str(result))

        elif user_input2 == '6':
            ing1 = float(input("Cabbege price? "))
            ing2 = float(input("Potato price? "))
            result = ((72 * ing1 + 72 * ing2) / 10)
            print("Price for one: " + str(result))

        else:
            print("Try again")

    elif user_input == 'pie':
            user_input2 = input("Choose pie tier (3, 5, 7): ")

            if user_input2 == '3':
                ing1 = int(input("Raw chicken meat price? "))
                ing2 = int(input("Flour price? "))
                ing3 = int(input("Wheat price? "))
                pie_t3(ing1, ing2, ing3)

            elif user_input2 == '5':
                ing1 = int(input("Raw goat meat price? "))
                ing2 = int(input("Flour price? "))
                ing3 = int(input("Cabbage price? "))
                ing4 = int(input("Goat milk price? "))
                pie_t5(ing1, ing2, ing3, ing4)

            elif user_input2 == '7':
                ing1 = int(input("Raw pork meat price? "))
                ing2 = int(input("Flour price? "))
                ing3 = int(input("Corn price? "))
                ing4 = int(input("Sheep milk price? "))
                pie_t7(ing1, ing2, ing3, ing4)

            else:
                print("Try again")

    else:
        print("Sth wrong mon!")



