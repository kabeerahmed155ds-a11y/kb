import math

def scientific_calculator():
    print("==== Full Featured Scientific Calculator ====")
    print("Available Operations:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    print("5. Power (x^y)")
    print("6. Square Root (√x)")
    print("7. Logarithm (log, log10)")
    print("8. Trigonometry (sin, cos, tan, radians, degrees)")
    print("9. Factorial (n!)")
    print("10. Exponential (e^x)")
    print("11. Exit")

    while True:
        choice = input("\nEnter operation number (1-11): ")

        try:
            if choice == "1":  # Addition
                a = float(input("Enter first number: "))
                b = float(input("Enter second number: "))
                print("Result:", a + b)

            elif choice == "2":  # Subtraction
                a = float(input("Enter first number: "))
                b = float(input("Enter second number: "))
                print("Result:", a - b)

            elif choice == "3":  # Multiplication
                a = float(input("Enter first number: "))
                b = float(input("Enter second number: "))
                print("Result:", a * b)

            elif choice == "4":  # Division
                a = float(input("Enter numerator: "))
                b = float(input("Enter denominator: "))
                if b == 0:
                    print("Error: Division by zero not allowed.")
                else:
                    print("Result:", a / b)

            elif choice == "5":  # Power
                a = float(input("Enter base: "))
                b = float(input("Enter exponent: "))
                print("Result:", math.pow(a, b))

            elif choice == "6":  # Square Root
                a = float(input("Enter number: "))
                print("Result:", math.sqrt(a))

            elif choice == "7":  # Logarithm
                a = float(input("Enter number: "))
                base = input("Enter base (e for natural log, 10 for log10): ")
                if base == "e":
                    print("Result:", math.log(a))
                else:
                    print("Result:", math.log10(a))

            elif choice == "8":  # Trigonometry
                func = input("Enter function (sin/cos/tan): ").lower()
                angle = float(input("Enter angle in degrees: "))
                rad = math.radians(angle)
                if func == "sin":
                    print("Result:", math.sin(rad))
                elif func == "cos":
                    print("Result:", math.cos(rad))
                elif func == "tan":
                    print("Result:", math.tan(rad))
                else:
                    print("Invalid function!")

            elif choice == "9":  # Factorial
                n = int(input("Enter integer: "))
                if n < 0:
                    print("Error: Factorial not defined for negative numbers.")
                else:
                    print("Result:", math.factorial(n))

            elif choice == "10":  # Exponential
                a = float(input("Enter number: "))
                print("Result:", math.exp(a))

            elif choice == "11":  # Exit
                print("Exiting calculator. Goodbye!")
                break

            else:
                print("Invalid choice. Please select from 1-11.")

        except ValueError:
            print("Invalid input! Please enter numeric values.")

# Run calculator
scientific_calculator()
