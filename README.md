# Grp7-Assignment1

## Question 1: Count Characters in a User-Inputted String

### Instructions:
Create a Student Management System function that:
- Combines all concepts to build a program which:
- Inputs student information (name, age, and grades for two or three courses)
- Calculates the average of the marks
- Stores and displays the student's information along with their average grade
- Uses separate functions for each operation (input, calculation, display)
The system should allow entering a student's name and their marks, then calculate and display the
student's average grade along with their name.

```python
def input_student_info():
    name = input("Enter student name: ")
    age = int(input("Enter student age: "))
    course1 = float(input("Enter marks for course 1: "))
    course2 = float(input("Enter marks for course 2: "))
    course3 = float(input("Enter marks for course 3 (or 0 if none): "))
    return {"name": name, "age": age, "courses": [course1, course2, course3]}

def calculate_average(marks):
    valid_marks = [mark for mark in marks if mark > 0]
    return sum(valid_marks) / len(valid_marks) if valid_marks else 0

def display_student_info(student):
    avg = calculate_average(student["courses"])
    print(f"\nStudent Information:")
    print(f"Name: {student['name']}")
    print(f"Age: {student['age']}")
    print(f"Marks: {student['courses']}")
    print(f"Average Grade: {avg:.2f}")

# Main program
student = input_student_info()
display_student_info(student)
```

## Question 2: Check Palindrome

### Instructions:
Write a function that asks the user to input a string and checks if the string is a palindrome (reads the
same forwards and backwards). Print "Yes, it is a palindrome" or "No, it is not a palindrome".

```python
def is_palindrome():
    text = input("Enter a word or phrase: ")
    # Remove spaces and convert to lowercase
    cleaned = text.replace(" ", "").lower()
    if cleaned == cleaned[::-1]:
        return "Yes - it's a palindrome!"
    else:
        return "No - it's not a palindrome."
```

