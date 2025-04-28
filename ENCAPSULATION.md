# Exp.No:6c
## Encapsulation

### AIM  
To write a Python program to create a class `Student` with the private members `name` and `age` and `roll no`, and an user defined function show() to display the details of the student ,use the getter and setter method Information Hiding and conditional logic for setting an object attributes.

### ALGORITHM

1. **Define the Class**  
   Create a class `Student` with a constructor (`__init__`) to initialize `name`, `roll_no`, and `age`. Make `roll_no` and `age` private by prefixing with double underscores (`__`).
2. **Initialize Attributes**  
   In the constructor, assign `name`, `__roll_no`, and `__age` to the object using `self`.
3. **Create `show()` Method**  
   Define a public method `show()` to print the student's name and roll number.
4. **Create Getter Method**  
   Define `get_roll_no()` to safely access the private `__roll_no` outside the class.
5. **Create Setter Method**  
   Define `set_roll_no(number)` to update the roll number only if it satisfies a condition.
6. **Add Validation in Setter**  
   In `set_roll_no`, check if `number > 50`; if yes, print an error, otherwise update `__roll_no`.
7. **Instantiate Object**  
   Create a `Student` object (`jessa`) with initial values for `name`, `roll_no`, and `age`.
8. **Use Getter/Setter Methods**  
   - Display original details with `show()`.
   - Attempt to update `roll_no` using `set_roll_no()`.
   - Re-display updated details using `show()`.
9. **End the program.**

### PROGRAM

```
class Student:
    def __init__(self, name, roll_no, age):
        # private member
        self.name = name
        self.__roll_no = roll_no
        self.__age = age

    def show(self):
        print('Student Details:', self.name, self.__roll_no)

    # getter methods
    def get_roll_no(self):
        return self.__roll_no

    # setter method to modify data member
    # condition to allow data modification with rules
    def set_roll_no(self,number):
        if number > 50:
            print('Invalid roll no. Please set correct roll number')
        else:
            self.__roll_no = number

jessa = Student('Jessa', 10, 15)

# before Modify
jessa.show()
# changing roll number as 120 using setter


jessa.set_roll_no(120)
jessa.set_roll_no(25)
jessa.show()
```

### OUTPUT
![image](https://github.com/user-attachments/assets/67b88298-1223-4066-ba33-eaf7847a472b)

### RESULT
Thus a Python program to create a class using encapsulation is implemented successfully.

