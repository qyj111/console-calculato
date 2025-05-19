def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero!")
    return a / b

def main():
    print("Console Calculator")
    print("Operations:")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")
    
    try:
        choice = int(input("Enter operation number (1-4): "))
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
        
        if choice == 1:
            result = add(num1, num2)
            print(f"Result: {num1} + {num2} = {result}")
        elif choice == 2:
            result = subtract(num1, num2)
            print(f"Result: {num1} - {num2} = {result}")
        elif choice == 3:
            result = multiply(num1, num2)
            print(f"Result: {num1} * {num2} = {result}")
        elif choice == 4:
            result = divide(num1, num2)
            print(f"Result: {num1} / {num2} = {result}")
        else:
            print("Invalid choice!")
    except ValueError as e:
        print(f"Error: {e}")

if __name__ == "__main__":
    main()
