# health_management
def gettime():
    import datetime
    return datetime.datetime.now()


def log():
    print("Choose your client")
    client = int(input("1. Kunal \n2. Rohit \n3. Akash"))
    con = 1
    if client == 1:
        while con == 1:
            print("What do you want to log for Kunal?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("Kunal diet.txt", "a")
                data = input("Enter what has Kunal Eaten?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()

            else:
                f = open("Kunal exercise.txt", "a")
                data = input("How much time has Kunal worked out?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()
            con = int(input("Do you want to log more for Kunal? \n1. Yes \n2. No"))

    elif client == 2:
        while con == 1:
            print("What do you want to log for Rohit?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("Rohit diet.txt", "a")
                data = input("Enter what has Rohit Eaten?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()

            else:
                f = open("Rohit exercise.txt", "a")
                data = input("How much time has Rohit worked out?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()
            con = int(input("Do you want to log more for Rohit? \n1. Yes \n2. No"))

    elif client == 3:
        while con == 1:
            print("What do you want to log for Akash?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("Akash diet.txt", "a")
                data = input("Enter what has Akash Eaten?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()

            else:
                f = open("Akash exercise.txt", "a")
                data = input("How much time has Akash worked out?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()
            con = int(input("Do you want to log more for Akash? \n1. Yes \n2. No"))


def retrieve():
    con = 1
    while con == 1:
        print("Choose your client")
        client = int(input("1. Kunal \n2. Rohit \n3. Akash"))
        if client == 1:
            print("What do you want to retrieve for Kunal?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("Kunal diet.txt", "r")
                print(f.readlines())
                f.close()

            else:
                f = open("Kunal exercise.txt", "r")
                print(f.readlines())
                f.close()

        elif client == 2:
            print("What do you want to retrieve for Rohit?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("Rohit diet.txt", "r")
                print(f.readlines())
                f.close()

            else:
                f = open("Rohit exercise.txt", "r")
                print(f.readlines())
                f.close()

        elif client == 3:
            print("What do you want to retrieve for Akash?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("Akash diet.txt", "r")
                print(f.readlines())
                f.close()

            else:
                f = open("hammad exercise.txt", "r")
                print(f.readlines())
                f.close()
    con = int(input("Do you want to retrieve any more details? \n1. Yes \n2. No"))


print("Welcome to Health care Management System")
ch = int(input("What do you want to do? \n1. Log \n2. Retrieve"))
if ch == 1:
    log()
elif ch == 2:
    retrieve()
else:
    print("Wrong Input. Please try again.")
