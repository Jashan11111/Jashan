def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)

result = factorial(5)
print("Factorial of 5:", result)

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):    
    return x * y

def divide(x, y):
    if y == 0:
        return "Error: Division by zero!"
    return x / y
# Example Python code to calculate the factorial of a number
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)

result = factorial(5)
print("Factorial of 5:", result)





# Example python code " Calculate Program" 
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):    
    return x * y

def divide(x, y):
    if y == 0:
        return "Error: Division by zero!"
    return x / y

while True:
    print("Options:")
    print("Enter 'add' for addition")
    print("Enter 'subtract' for subtraction")
    print("Enter 'multiply' for multiplication")
    print("Enter 'divide' for division")
    print("Enter 'exit' to end the program")

    user_input = input(": ")

    if user_input == "exit":
        break
    elif user_input in ["add", "subtract", "multiply", "divide"]:
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
        if user_input == "add":
            print("Result:", add(num1, num2))
        elif user_input == "subtract":
            print("Result:", subtract(num1, num2))
        elif user_input == "multiply":
            print("Result:", multiply(num1, num2))
        elif user_input == "divide":
            print("Result:", divide(num1, num2))
    else:
        print("Invalid input")





# python code for guess the number game
import random

target_number = random.randint(1, 100)
attempts = 0

print("Welcome to the Guess the Number game!")
print("I'm thinking of a number between 1 and 100.")

while True:
    guess = int(input("Take a guess: "))
    attempts += 1

    if guess < target_number:
        print("Too low! Try again.")
    elif guess > target_number:
        print("Too high! Try again.")
    else:
        print(f"Congratulations! You guessed the number {target_number} in {attempts} attempts.")
        break




# python code for simple weather app
weather_data = {
    "Monday": "Sunny",
    "Tuesday": "Rainy",
    "Wednesday": "Cloudy",
    "Thursday": "Sunny",
    "Friday": "Windy",
    "Saturday": "Rainy",
    "Sunday": "Sunny"
}

while True:
    day = input("Enter a day of the week (or 'exit' to end): ").capitalize()

    if day == "Exit":
        break

    if day in weather_data:
        print(f"The weather on {day} is {weather_data[day]}.")
    else:
        print("Invalid input. Please enter a valid day of the week.")

        # Example code: Quick Sort algorithm
# I find this code inspiring because it's an efficient sorting algorithm
# that I want to learn from and possibly implement in my projects.
def quicksort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quicksort(left) + middle + quicksort(right)


    #This program converts temperatures between Celsius and Fahrenheit
def celsius_to_fahrenheit(celsius):
    fahrenheit = (celsius * 9/5) + 32
    return fahrenheit

def fahrenheit_to_celsius(fahrenheit):
    celsius = (fahrenheit - 32) * 5/9
    return celsius

choice = input("Convert to Celsius (C) or Fahrenheit (F)? ").upper()
temperature = float(input("Enter temperature value: "))

if choice == "C":
    converted_temp = fahrenheit_to_celsius(temperature)
    print(f"{temperature}°F is equal to {converted_temp}°C")
elif choice == "F":
    converted_temp = celsius_to_fahrenheit(temperature)
    print(f"{temperature}°C is equal to {converted_temp}°F")
else:
    print("Invalid choice. Please enter C or F.")


#This program allows users to create and manage a simple to-do list.
to_do_list = []

while True:
    print("To-Do List:")
    for i, task in enumerate(to_do_list, 1):
        print(f"{i}. {task}")

    choice = input("Enter 'A' to add a task, 'D' to delete a task, or 'Q' to quit: ").upper()

    if choice == "A":
        task = input("Enter a new task: ")
        to_do_list.append(task)
    elif choice == "D":
        task_index = int(input("Enter the task number to delete: ")) - 1
        if 0 <= task_index < len(to_do_list):
            del to_do_list[task_index]
        else:
            print("Invalid task number.")
    elif choice == "Q":
        break
    else:
        print("Invalid choice. Please enter A, D, or Q.")
