# rock-paper-scissor-game


import random

def rockgame(comp , you):
    if comp ==  you:
        return None
    elif comp == 'rock':
        if you == 'paper':
            return False
        if you == 'scissor':
            return True
    elif comp == 'paper':
        if you == 'scissor':
            return False
        if you == 'rock':
            return True
    elif comp == 'scissor':
        if you == 'rock':
            return False
        if you == 'paper':
            return True


print("computer turn : choose Rock , Paper , Scissor")
comp = ("your turn : choose rock , paper , scissor :")

randomno = random.randint(1,3)
if randomno == 1:
    comp = 'rock'
if randomno == 2:
    comp = 'paper'
if randomno == 3:
    comp = 'scissor' 
       
you = input("muskan Turn : choose rock , paper , scissor : ")
a = rockgame(comp , you)

print(f"computer chose {comp}")
print(f"you chose {you}")

if a == None:
    print("this game is a tie")
elif a:
    print("you lose!")
else:
    print("you win")
