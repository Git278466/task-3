# task-3
import random

def generate_password(length):
    if length < 1:
        print("Password length must be at least 1.")
        return None  # Return None if the length is invalid

    all_characters = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*()"
    password = ''.join(random.choices(all_characters, k=length))
    return password  # Return the generated password

# Example usage
length = int(input("Enter password length: "))
password = generate_password(length)

if password:  # Only print if a valid password was generated
    print(f"Generated Password: {password}")
