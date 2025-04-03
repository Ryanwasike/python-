# python-
for plp wk 1 assignment


# Simple Calculator Program

def perform_operation(num1, num2, operation):
    if operation == '+':
        return num1 + num2
    elif operation == '-':
        return num1 - num2
    elif operation == '*':
        return num1 * num2
    elif operation == '/':
        if num2 != 0:
            return num1 / num2
        else:
            return "Error: Division by zero"
    else:
        return "Error: Invalid operation"

def main():
    print("Welcome to the Simple Calculator!")
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
        operation = input("Enter the operation (+, -, *, /): ")

        result = perform_operation(num1, num2, operation)

        if isinstance(result, str) and "Error" in result:
            print(result)
        else:
            print(f"{num1} {operation} {num2} = {result}")
    except ValueError:
        print("Error: Please enter valid numbers.")

if __name__ == "__main__":
    main()

