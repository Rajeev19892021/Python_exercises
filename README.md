# Python_exercises
#Ex_1:Apni dictionary
# First program in the dictionary
oxford = {"Apple":"It is a fruit", "Lady Finger":"It is type of vegitables", "Truth":"Fact", "Lie":"one is not true"}
print("Please enter words from the following: ")
print("Apple,Lady Finger,Truth,Lie: ")
a = input()
print("menaing is: ", oxford.get(a, "Meaning is not defined in the dictionary"))

#Ex_2 


#Faulty Calculator
op = input("Please enter the operation +,-,*,/: ")
print("Operation is: ", op)
print("Please enter two numbers")
a = int(input())
b = int(input())

if op=='+':
    if a==56 and b==9:
        print("Addition is:77")
    else:
        print(a + b)
elif op=='-':
    print(a - b)
elif op=='*':
    if a==45 and b==3:
        print("Multiplication is: 555")
    else:
        print(a * b)
elif op=='/':
    if a==56 and b==6:
        print("devision is: 4")
    else:
        print(a / b)

Ex_3: Guess the number


#no of gueses
#print no of guesses left
#no of guesses he took to finish
#game over
n = 20
i = 1
while(i<=9):
    inp = int(input("Please guess the number between 1 to 50: "))
    if(inp==n):
        print("Congratulations! you have guess the right number ")
        print("You have taken chances to finish: ",i)
        break
    else:
        left = 9 - i
        i = i + 1

        print("Chances left: ",left)
        if left == 0:
            print("Game Over\n")
            print("You have lost all the chances! Please try again ")
            break
        if inp>n:


            print("Please enter lesser number")
        else:
            print("Please enter greater number")
        continue

#Ex_4:
n = int(input("Enter a number: "))
b = bool(int(input("Enter 1 or 0: ")))
if b==bool(1):

    row=0
    star=0
    while row<n:

        star = row + 1
        while star>0:
            print('*', end=" ")
            star = star -1
        row = row + 1
        print()
else:
    row = 0
    star = 0
    while row<n:
        star = n -row
        while star>0:
            print('*',end=" ")
            star = star -1
        row = row + 1
        print()

#Ex_5: Health Management System
#Helath Managemnet system
#3 clients - Raju, Aviral, Pranav
#6 files (3-excersize and 3 - food)
def getdate():
    import datetime
    return datetime.datetime.now()

def retrieve(s, a):
    if s=="Raju":
        if a==1:
            f = open("Raju_Ex.txt")
            print(f.read())
            f.close()
        else:
            f = open("Raju_Food.txt")
            print(f.read())
            f.close()
    elif s=="Aviral":

        if a==1:

            f1 = open("Aviral_Ex.txt")
            print(f1.read())
            f1.close()
        else:
            f1 = open("Aviral_Food.txt")
            print(f1.read())
            f1.close()

    elif s=="Pranav":

        if a==1:
            f2 = open("Pranav_Ex.txt")
            print(f2.read())
            f2.close()
        else:
            f2 = open("Pranav_Food.txt")
            print(f2.read())
            f2.close()






def health_system(s):

        if s==1:
            print("What you want to do: \n"
                   "1. Log\n"
                   "2. Retrieve\n")
            a = int(input())

            # a = int(input(print("What you want to do: \n"
            #       "1. Log\n"
            #       "2. Retrieve\n")))

            if a==1:
                b = int(input("What you want to Log\n"
                              "1 - Exercise\n"
                              "2 - Food\n"))

                if b==1:
                    str1 = input("Enter details: \n")
                    f = open("Raju_Ex.txt", "a")


                    f.write("[" + str(getdate()) + "]:" + str1)
                    f.write("\n")
                    f.close()
                    return print("You have Logged Exercise successfully: Raju")
                else:
                    str1 = input("Enter details: \n")
                    f = open("Raju_Food.txt", "a")

                    f.write("[" + str(getdate()) + "]:" + str1)
                    f.write("\n")
                    f.close()
                    return print("You have Logged diet successfully for: Raju")


            else:

                b = int(input("What you want to Retrieve\n"
                                  "1 - Exercise\n"
                                  "2 - Food\n"))
                if b==1:
                    retrieve("Raju", 1)
                else:
                    retrieve("Raju", 2)

        elif s==2:
            print("What you want to do log or Retrieve for Aviral: \n"
                   "1. Log\n"
                   "2. Retrieve\n")
            b = int(input())
            # b = int(input(print("What you want to do log or Retrieve for Aviral: \n"
            #       "1. Log\n"
            #       "2. Retrieve\n")))
            if b==1:
                c = int(input("What you want to Log\n"
                              "1 - Exercise\n"
                              "2 - Food\n"))
                if c==1:
                    str2 = input("Enter Details: ")
                    f = open("Aviral_Ex.txt", "a")

                    f.write("[" + str(getdate()) + "]:" + str2)
                    f.write("\n")
                    f.close()
                    return print("You have Logged Exercise successfully for: Aviral")
                else:
                    str2 = input("Enter Details: ")
                    f = open("Aviral_Food.txt", "a")

                    f.write("[" + str(getdate()) + "]:" + str2)
                    f.write("\n")
                    f.close()
                    return print("You have Logged diet successfully for: Aviral")

            else:
                c = int(input("What you want to Retrieve\n"
                              "1 - Exercise\n"
                              "2 - Food\n"))
                if c == 1:
                    retrieve("Aviral", 1)
                else:
                    retrieve("Aviral", 2)

        elif s==3:
            print("What you want to do log or Retrieve for Pranav: \n"
                                 "1. Log\n"
                                 "2. Retrieve\n")
            d = int(input())
            # d = int(input(print("What you want to do log or Retrieve for Pranav: \n"
            #                     "1. Log\n"
            #                     "2. Retrieve\n")))
            if d == 1:
                e = int(input("What you want to Log\n"
                              "1 - Exercise\n"
                              "2 - Food\n"))
                if e == 1:
                    str3 = input("Enter Details: ")
                    f = open("Pranav_Ex.txt", "a")

                    f.write("[" + str(getdate()) + "]:" + str3)
                    f.write("\n")
                    f.close()
                    return print("You have Logged Exercise successfully for: Pranav ")
                else:
                    str3 = input("Enter Details: ")
                    f = open("Pranav_Food.txt", "a")

                    f.write("[" + str(getdate()) + "]:" + str3)
                    f.write("\n")
                    f.close()
                    return print("You have Locked diet successfully for: Pranav ")

            else:
                c = int(input("What you want to Retrieve\n"
                              "1 - Exercise\n"
                              "2 - Food\n"))
                if c == 1:
                    retrieve("Pranav", 1)
                else:
                    retrieve("Pranav", 2)



        else:
            return print("Please enter valid input: ")






name = int(input("********************************\n"
    "Please enter client's name: \n"
                 "********************************\n"
             "Type 1 - Raju\n"
             "Type 2 - Aviral\n"
             "Type 3 - Pranav\n"
              "********************************\n"))
health_system(name)

#Ex_6: Snake Water Gun Game 
#Snake Water Gun
import random
list1 = ["snake", "water", "Gun"]
#random.choice(list1)
i = 0
your_points = 0
Computer_points = 0
print("You have total 10 chances to win this game")
while i<10:
    choice = random.choice(list1)

    inp = input("Please enter Snake/Water/Gun:s/w/g: ")
    if choice=="snake" and inp=="w":
        Computer_points += 1
        print("You have lost this chance! \nComputer points: ", Computer_points)
        print("Your points:", your_points)
    elif choice=="water" and inp=="s":
        your_points += 1
        print("Yo have won this chnace! \nComputer points: ", Computer_points)
        print("Your points:", your_points)
    elif choice=="snake" and inp=="g":
        your_points += 1
        print("Yo have won this chnace! \nComputer points: ", Computer_points)
        print("Your points:", your_points)
    elif choice=="Gun"and inp=="s":
        Computer_points += 1
        print("You have lost this chance! \nComputer points: ", Computer_points)
        print("Your points: ", your_points)
    elif choice=="water" and inp=="g":
        Computer_points += 1
        print("You have lost this chance! \nComputer points: ", Computer_points)
        print("Your points: ", your_points)
    elif choice=="Gun"and inp=="w":
        your_points += 1
        print("You have won this chance! \nComputer points: ", Computer_points)
        print("Your points:", your_points)
    elif (choice=="snake" and inp=="s") or (choice=="water" and inp=="w") or (choice=="Gun" and inp=="g"):
        Computer_points += 0
        your_points += 0
        print("No one has won this chance! \nComputer points: ", Computer_points)
        print("Your points: ", your_points)
    else:
        print("Invalid input entered")

    chances_left = 9 -i
    if chances_left==0:
        break
    i = i + 1
    print("You have " + str(chances_left) + " chances left")

if Computer_points>your_points:
    print("You have lost the Game")

elif Computer_points<your_points:
    print("Congratulations! You have Won the Game")

else:
    print("It's a tie: ")
















