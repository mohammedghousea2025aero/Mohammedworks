# Mohammedworks
Python projecta
# Number Guessing Game
# Author: Mohammed Ghouse

import random

def game():
    print("Welcome to Number Guessing Game!")
    print("I'm thinking of a number between 1 and 20.")

    number = random.randint(1, 20)
    attempts = 0

    while True:
        guess = input("Take a guess: ")

        # Check if input is a number
        if not guess.isdigit():
            print("Please enter a valid number.")
            continue

        guess = int(guess)
        attempts += 1

        if guess < number:
            print("Too low! Try again.")
        elif guess > number:
            print("Too high! Try again.")
        else:
            print(f"Congratulations! You guessed the number {number} in {attempts} attempts.")
            break

# Start the game
if __name__ == "__main__":
    game()
