# Example Site
                                        Snake Gun and Water Game

Here is one of the most simple way to create Snake water Gun game. Hope you all will like my method
#My Name is Tauheed Shaikh and This my First project on github
def SnakeGame():
    """I think you Know how to play snake water gun game"""
    import random
    list = ["s","g","w"]
    you = 0
    computer = 0
    for i in range(0,10):
        user_choice = input("This is a Snake,Water,Gun game For eg. if computer choose snake and you "
        "choose water then Computer will win and so on hope you will enjoy this game Select s.Snake g.Gun"
        " w.Water\n")
        print("your choice",user_choice)
        Computer_choice = random.choice(list)
        print("computer choice",Computer_choice)
        print("Your Life is",10 - i)
        if user_choice == Computer_choice:
         print("tie")
        elif user_choice == 's' and Computer_choice == 'w':
         you +=1
         #print("You win")
         print(f"You won {you}")

        elif user_choice == 'w' and Computer_choice == 's':
         #print("You lost")
         computer += 1
         print(f"You lost {computer}")

        elif user_choice == 'w' and Computer_choice == 'g':
         #print("You won")
         you += 1
         print(f"You won {you}")
        elif user_choice == 'g' and Computer_choice == 'w':
         # print("You lost")
         computer += 1
         print(f"You lost {computer}")
        elif user_choice == 'g' and Computer_choice == 's':
         #print("You won")
         you +=1
         print(f"You lost {you}")
        elif user_choice == 's' and Computer_choice == 'g':
         #print("You lost")
         computer += 1
         print(f"You lost {computer}")
        else:
            print("Invalid input,Please see whether you have typed s which is for Snake w for Water g for Gun if not it will show invalid input")
    if you > computer:
     print("You have won this game vs computer,Winner Winner Chicken Dinner")
    else:
     print("Sorry,You have lost this game with Computer")
SnakeGame()

Repeat_game = int(input("Select 1.If you want to repeat this game again and 2.Exit\n"))
if Repeat_game == 1:
    SnakeGame()
else:
    print("See you Again Later")