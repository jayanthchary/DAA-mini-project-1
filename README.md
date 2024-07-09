import random

def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    x = int(input("Enter the lower bound of the range: "))
    y = int(input("Enter the upper bound of the range: "))
    number = random.randint(x, y)
    attempts = 0

    while True:
        guess = int(input(f"Guess a number between {x} and {y}: "))
        attempts += 1

        if guess < number:
            print("Too low, try again.")
        elif guess > number:
            print("Too high, try again.")
        else:
            print(f"Congratulations! You guessed the number {number} correctly in {attempts} attempts.")
            break

number_guessing_game()
