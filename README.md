# password
import random
import string

def g_p(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

def main():
    try:
        length = int(input("Enter the desired password length: "))
        if length <= 0:
            print("Password length should be a positive integer.")
            return
        password = g_p(length)
        print("Generated Password:", password,"\nThanks your password were generated successfully...")
    except ValueError:
        print("Invalid input. Please enter a valid positive integer.")

if __name__ == "__main__":
    main()
