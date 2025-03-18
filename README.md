# PythonAssignment
Writing code for a calculator
def calculator():
    try:
        # Ask for numbers
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
        
        # Ask for operation
        operation = input("Enter operation (+, -, *, /): ")
        
        # Do the math
        if operation == '+':
            result = num1 + num2
        elif operation == '-':
            result = num1 - num2
        elif operation == '*':
            result = num1 * num2
        elif operation == '/':
            if num2 != 0:
                result = num1 / num2
            else:
                print("Error: Cannot divide by zero.")
                return
        else:
            print("Invalid operation! Use +, -, *, or /.")
            return
        
        # Show the result
        print(f"{num1} {operation} {num2} = {result}")
    
    except ValueError:
        print("Invalid input! Enter numbers only.")

# Run the calculator
calculator()
