FACTORIAL
WORKFLOW
1.	Start
2.	Input number n
3.	Check if n < 0
If yes → print error (factorial not defined) → End
4.	Set result = 1
5.	Loop from 1 to n
6.	Display 
7.	End

PSEUDO CODE
BEGIN
	INPUT n

	IF n < O THEN
		PRINT “Factorial not defined for negative numbers”
	ELSE
		SET result = 1

		FOR i = 1 TO n DO
			result = result * 1
		END FOR

PRINT result
END IF

END






PYTHON CODE
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
    print("\nFactorial Calculator")
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
