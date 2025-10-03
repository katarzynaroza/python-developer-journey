# 📝 Task - write a function students_with_min_grade that:  
- takes the dictionary class_register,  
- returns a list of students with the lowest grades in the class.

RESULT:  
<pre>
def students_with_min_grade(class_register: dict) -> list:

    min_students = []
    if class_register == {}:
        return None
    min_value = min(class_register.values())

    for name, grade in class_register.items():
        if grade == min_value:
            min_students.append(name)
    return min_students

class_register = {}
print(students_with_min_grade(class_register))
</pre>

# 💭 Technical reflection: 
- At the beginning my code, looked like that:
<pre>
def students_with_min_grade(class_register: dict) -> list:
    min_students = []
  
    for name, grade in class_register.items():
    min_value = min(class_register.values())
        if grade == min_value:
            min_students.append(name)
    return min_students

class_register = {}
print(students_with_min_grade(class_register))
</pre>
- In this code, there was wasting of time, because each time it looks for the minimum in the entire list of grades → this is unnecessary repetition of calculations.
- In this code function doesn't work with empty dictionary.
- Furthermore, first when I added support for the edge case, I aded like that:
<pre>
if class_register == {}:
    min_students = []
min_value = min(class_register.values())
</pre>
- In this case function doesn't work (it tried to count a min function with empty dictionary), because it doesn't return anything. I had to replace "min_students = []" with "return None" or "return []".  
