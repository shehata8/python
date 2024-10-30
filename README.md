# python
import random
rock =("""
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
""")
paper =("""
     _______
---'    ____)____
           ______)
          _______)
         _______)
---.__________)
""")
scissors =("""
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
""")
print("welcome to paper , rock , scissors game")
ask = input("please press Enter to play or type (Help) for the rules help:\n").lower()
if ask == "help" :
 print("""
                          ............RULES............
                          1)YOU CHOOSE AND THE COMPUTER CHOOSES
                          2)ROCK SMASHES SCISSORS -> ROCK WINS
                          3)SCISSORS CUT PAPER -> SCISSORS WIN
                          4) PAPER COVERS ROCK -> PAPER WIN
                           """)
choose = input("please choose (Rock , Paper , scissors)\n").lower()
computer_choose = random.choice(["rock","paper","scissors"])
if choose == computer_choose :
 print(" it's draw ")
elif (choose == "rock" and computer_choose == "paper") or (choose == "rock" and computer_choose == "scissors") or (choose == "paper" and computer_choose == "rock") :
 print(" you win ")
elif choose not in ["rock","paper","scissors"]:
 print("WRONG")
else:
 print(" you lose ")
if choose == "rock":
 print(f"you chose (rock)\n{rock}")
elif choose == "paper":
 print(f"you chose (paper)\n{paper}")
elif choose == "scissors":
 print(f"you chose (scissors)\n{scissors}")
else:
 print("error")
if computer_choose == "rock":
 print(f"computer chose (rock)\n{rock}")
elif computer_choose == "paper":
 print(f"computer chose (paper)\n{paper}")
else:
 print(f"computer chose (scissors)\n{scissors}")

