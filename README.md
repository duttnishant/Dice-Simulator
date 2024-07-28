import random

def roll_dice(sides=6):
    return random.randint(1, sides)

def main():
    print("Welcome to the Dice Simulator!")
    
    while True:
        sides = input("press ENTER to get a random dice number: ")
        if sides.isdigit():
            sides = int(sides)
        else:
            sides = 6
        
        roll_again = "yes"
        while roll_again.lower() in ["yes", "y"]:
            result = roll_dice(sides)
            print(f"You rolled a {result}.")
            
            roll_again = input("Do you want to roll again? (yes/no): ")
        
        play_again = input("Do you want to use another dice? (yes/no): ")
        if play_again.lower() not in ["yes", "y"]:
            print("Thank you for playing DICE SIMULATOR!")
            break

if __name__ == "__main__":
    main()
