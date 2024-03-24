import random
import string

def generate_password(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choices(characters, k=length))
    return password

def print_banner():
    banner = """
    _______  __   __  _______  ______    _______  __   __  _______ 
   |       ||  | |  ||       ||    _ |  |       ||  | |  ||       |
   |    _  ||  |_|  ||    ___||   | ||  |    ___||  | |  ||  _____|
   |   |_| ||       ||   |___ |   |_||_ |   |___ |  |_|  || |_____ 
   |    ___||_     _||    ___||    __  ||    ___||       ||_____  |
   |   |      |   |  |   |___ |   |  | ||   |___ |       | _____| |
   |___|      |___|  |_______||___|  |_||_______||_______||_______|

   """
    print(banner)

def main():
    print_banner()
    print("Welcome to the Unique Password Generator!")
    print("------------------------------------------------")

    try:
        length = int(input("Enter the desired length of the password: "))
        if length <= 0:
            print("Invalid length. Please enter a positive integer.")
            return

        password = generate_password(length)

        print("Your generated password is:")
        print(password)
    except ValueError:
        print("Invalid input. Please enter a valid integer for the length.")

if __name__ == "__main__":
    main()

