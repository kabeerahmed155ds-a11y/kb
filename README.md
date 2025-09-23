import math

def scientific_calculator():
    print("\n==== Scientific Calculator ====")
    print("Available operations:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    print("5. Modulus (%)")
    print("6. Power (x^y)")
    print("7. Square Root (√)")
    print("8. Sine (sin)")
    print("9. Cosine (cos)")
    print("10. Tangent (tan)")
    print("11. Logarithm (log base 10)")
    print("12. Natural Logarithm (ln)")
    print("13. Exponential (e^x)")
    print("14. Factorial (n!)")
    print("15. Exit")

    while True:
        choice = input("\nEnter operation number (1-15): ")

        if choice == '1':
            a = float(input("Enter first number: "))
            b = float(input("Enter second number: "))
            print("Result =", a + b)

        elif choice == '2':
            a = float(input("Enter first number: "))
            b = float(input("Enter second number: "))
            print("Result =", a - b)

        elif choice == '3':
            a = float(input("Enter first number: "))
            b = float(input("Enter second number: "))
            print("Result =", a * b)

        elif choice == '4':
            a = float(input("Enter numerator: "))
            b = float(input("Enter denominator: "))
            if b != 0:
                print("Result =", a / b)
            else:
                print("Error! Division by zero.")

        elif choice == '5':
            a = int(input("Enter first number: "))
            b = int(input("Enter second number: "))
            print("Result =", a % b)

        elif choice == '6':
            a = float(input("Enter base: "))
            b = float(input("Enter exponent: "))
            print("Result =", math.pow(a, b))

        elif choice == '7':
            a = float(input("Enter number: "))
            print("Result =", math.sqrt(a))

        elif choice == '8':
            angle = float(input("Enter angle in degrees: "))
            print("Result =", math.sin(math.radians(angle)))

        elif choice == '9':
            angle = float(input("Enter angle in degrees: "))
            print("Result =", math.cos(math.radians(angle)))

        elif choice == '10':
            angle = float(input("Enter angle in degrees: "))
            print("Result =", math.tan(math.radians(angle)))

        elif choice == '11':
            a = float(input("Enter number: "))
            print("Result =", math.log10(a))

        elif choice == '12':
            a = float(input("Enter number: "))
            print("Result =", math.log(a))

        elif choice == '13':
            a = float(input("Enter exponent: "))
            print("Result =", math.exp(a))

        elif choice == '14':
            a = int(input("Enter integer: "))
            print("Result =", math.factorial(a))

        elif choice == '15':
            print("Exiting calculator... Goodbye!")
            break

        else:
            print("Invalid input! Please choose between 1-15.")

# Run program
scientific_calculator()
