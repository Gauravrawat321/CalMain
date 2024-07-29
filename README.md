# CalMain
import math

def calculator():
    print("Complex Calculator")
    print("Available operations:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    print("5. Power (^)")
    print("6. Square Root (sqrt)")
    print("7. Logarithm (log)")
    print("8. Sine (sin)")
    print("9. Cosine (cos)")
    print("10. Tangent (tan)")
    print("11. Exit")

    while True:
        choice = input("\nEnter the operation: ")

        if choice == '11':
            print("Exiting the calculator. Goodbye!")
            break

        try:
            if choice in ['1', '2', '3', '4', '5']:
                num1 = float(input("Enter the first number: "))
                num2 = float(input("Enter the second number: "))

            if choice == '1':
                print(f"Result: {num1 + num2}")
            elif choice == '2':
                print(f"Result: {num1 - num2}")
            elif choice == '3':
                print(f"Result: {num1 * num2}")
            elif choice == '4':
                print(f"Result: {num1 / num2}")
            elif choice == '5':
                print(f"Result: {math.pow(num1, num2)}")
            elif choice == '6':
                num = float(input("Enter the number: "))
                print(f"Result: {math.sqrt(num)}")
            elif choice == '7':
                num = float(input("Enter the number: "))
                base = float(input("Enter the base (default is e): ") or math.e)
                print(f"Result: {math.log(num, base)}")
            elif choice == '8':
                angle = float(input("Enter the angle in degrees: "))
                print(f"Result: {math.sin(math.radians(angle))}")
            elif choice == '9':
                angle = float(input("Enter the angle in degrees: "))
                print(f"Result: {math.cos(math.radians(angle))}")
            elif choice == '10':
                angle = float(input("Enter the angle in degrees: "))
                print(f"Result: {math.tan(math.radians(angle))}")
            else:
                print("Invalid operation")
        except ValueError:
            print("Invalid input. Please enter numerical values.")
        except ZeroDivisionError:
            print("Error: Division by zero is not allowed.")
        except Exception as e:
            print(f"An error occurred: {e}")

if __name__ == "__main__":
    calculator()
