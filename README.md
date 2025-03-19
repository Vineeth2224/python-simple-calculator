# Simple Python Calculator

# Function to add two numbers
def add(x, y):
    return x + y

# Function to subtract two numbers
def subtract(x, y):
    return x - y

# Function to multiply two numbers
def multiply(x, y):
    return x * y

# Function to divide two numbers
def divide(x, y):
    if y != 0:
        return x / y
    else:
        return "Error! Division by zero."

# Main program loop
def calculator():
    print("Welcome to the Simple Python Calculator!")
    print("Available operations:")
    print("1. Add (+)")
    print("2. Subtract (-)")
    print("3. Multiply (*)")
    print("4. Divide (/)")

    while True:
        # Input choice
        choice = input("\nEnter choice (1/2/3/4) or 'q' to quit: ")

        # Exit the program
        if choice == 'q':
            print("Exiting the calculator. Goodbye!")
            break
        
        if choice not in ('1', '2', '3', '4'):
            print("Invalid input. Please try again.")
            continue

        # Input numbers
        try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
        except ValueError:
            print("Invalid input. Please enter valid numbers.")
            continue

        # Perform the calculation based on user choice
        if choice == '1':
            print(f"The result of {num1} + {num2} is {add(num1, num2)}")
        elif choice == '2':
            print(f"The result of {num1} - {num2} is {subtract(num1, num2)}")
        elif choice == '3':
            print(f"The result of {num1} * {num2} is {multiply(num1, num2)}")
        elif choice == '4':
            print(f"The result of {num1} / {num2} is {divide(num1, num2)}")

if __name__ == "__main__":
    calculator()

