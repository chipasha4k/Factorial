# Factorial

def factorial_with_steps(n):
    if n < 0:
        return None

    result = 1
    steps = ""

    for i in range(1, n + 1):
        result *= i
        steps += str(i)
        if i < n:
            steps += " × "

    return result, steps


while True:
    print("\n=== Factorial Calculator (With Steps) ===")
    
    user_input = input("Enter a number (or type 'exit' to quit): ")

    if user_input.lower() == 'exit':
        print("Goodbye!")
        break

    if not user_input.isdigit():
        print("Invalid input. Please enter a positive integer.")
        continue

    num = int(user_input)
    answer = factorial_with_steps(num)

    if answer is None:
        print("Factorial not defined for negative numbers.")
    else:
        result, steps = answer
        print(f"\nWorking:")
        print(f"{num}! = {steps}")
        print(f"{num}! = {result}")
