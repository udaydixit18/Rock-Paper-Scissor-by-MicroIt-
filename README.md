# Rock-Paper-Scissor-by-MicroIt-
import random

def rock_paper_scissors():
    options = ["rock", "paper", "scissors"]
    rounds = int(input("How many rounds would you like to play? "))
    user_score = 0
    computer_score = 0

    for i in range(rounds):
        print(f"\nRound {i+1}")
        user_choice = input("Choose rock, paper, or scissors: ").lower()
        if user_choice not in options:
            print("Invalid choice, try again.")
            continue

        computer_choice = random.choice(options)
        print(f"Computer chose: {computer_choice}")

        if user_choice == computer_choice:
            print("It's a tie!")
        elif (user_choice == "rock" and computer_choice == "scissors") or \
             (user_choice == "paper" and computer_choice == "rock") or \
             (user_choice == "scissors" and computer_choice == "paper"):
            print("You win this round!")
            user_score += 1
        else:
            print("Computer wins this round!")
            computer_score += 1

    print(f"\nFinal Score: You {user_score} - Computer {computer_score}")
    if user_score > computer_score:
        print("You won the game!")
    elif user_score < computer_score:
        print("Computer won the game!")
    else:
        print("It's a draw!")

if __name__ == "__main__":
    rock_paper_scissors()
