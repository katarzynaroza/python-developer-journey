# 📝 Task - Write a function best_student that: takes a dictionary class register (keys: names, values: grades), returns the name of the student with the highest grade.  
  
RESULT:  
<pre>
def best_student(class_register: dict) -> str | None:
    if not class_register:
        return None
    best_name = list(class_register)[0]              # best_name and best_grade should refer to the same student from the start. If I set best_name = "" and best_grade = 0, they don't represent any real student. I then have a "false record" and have to do additional combinations to correct it later.  
    best_grade = list(class_register.values())[0]    # In the loop, I compare if grade > best_grade: If best_grade were empty ("", None, 0 only as a placeholder), the comparison doesn't always make sense  

    for name, grade in class_register.items():
        if grade > best_grade:
            best_grade = grade
            best_name = name
        elif grade == best_grade:
            best_name = min([name, best_name])

    return best_name

class_register = {"Emma": 3, "Klaudia": 5, "Zuzanna": 4}
print(best_student(class_register))
</pre>

# 💭 Technical reflection: 
- An empty variable that has digits: x = 0 or x = int(). 

# 🔖 Tags / topics:
`TAG: items() | TAG: dictionary`
