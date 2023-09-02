import random

def get_user_input(prompt):
    return int(input(prompt))

def generate_number():
    return random.randint(100, 999)  # You can adjust the range as needed

def get_matching_digits(secret_number, guess):
    return sum([1 for s, g in zip(str(secret_number), str(guess)) if s == g])

def main():
    print("Welcome to the Mastermind game!")
    
    player1_number = generate_number()
    print("Player 1, you have set your number.")
    
    attempts = 0
    while True:
        player2_guess = get_user_input("Player 2, take a guess: ")
        attempts += 1
        
        if player2_guess == player1_number:
            print(f"Congratulations! Player 2 wins in {attempts} attempts!")
            break
        else:
            matching_digits = get_matching_digits(player1_number, player2_guess)
            print(f"Correct digits: {matching_digits}")
    
    print("\nPlayer 2's turn to set the number!")
    player2_number = get_user_input("Player 2, set your number: ")
    
    attempts = 0
    while True:
        player1_guess = generate_number()
        attempts += 1
        
        if player1_guess == player2_number:
            print(f"Congratulations! Player 1 wins in {attempts} attempts!")
            break
    
    print(f"Player 2's number was: {player2_number}")
    print("Game over.")

if __name__ == "__main__":
    main()
