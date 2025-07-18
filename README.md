# Python-Rock-Paper-Scissor-Game
import random
def rock_paper_Scissor(comp,you):
    if comp==you:
        return None
    elif comp=="r":
        if you=="p":
            return True
        elif you=="s":
            return False
    elif comp=="p":
        if you=="s":
            return True
        elif you=="r":
            return False
    elif comp=="s":
        if you=="r":
            return True
        elif you=="p":
            return False
        
print("Computer's turn: choose Rock (r), Paper(p), or Scissor(s):")
computer=" "
randNo=random.randint(1,3)
if randNo==1:
    computer="s"
elif randNo==2:
    computer="r"
elif randNo==3:
    computer="p"

you=input("Your turn: choose Rock (r), Paper(p), or Scissor(s):")

a=rock_paper_Scissor(computer,you)
print(f"Computer choose:{computer}")
print(f"You choose:{you}")

if a:
    print("You Win!")
elif a is None:
    print("This is a tie!")
else:
    print("You Lose!")
