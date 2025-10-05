# 📝 Task - wite a most_common_grade key that:
- takes a class_register dictionary.  
- returns the most common rating.  
- if there is a tie, return the lowest rating among the most common.
<pre>
RESULT:  
def most_common_grade(class_register: dict) -> int:
    class_grades = list(class_register.values())
    grades_number = {}
    for grade in class_grades:
        grades_number[grade] = class_grades.count(grade)

    most_often_key = [list(grades_number)[0]]
    most_often_value = list(grades_number.values())[0]
    for key, value in grades_number.items():
        if value > most_often_value:
            most_often_key = [key]
        elif value == most_often_value:
            most_often_key.append(key)
    return min(most_often_key)

class_register = {"Joanna": 5, "Magdalena": 3, "Zuzanna": 5, "Ewelina": 3, "Michalina": 1}
print(most_common_grade(class_register)) 
# 3
</pre>    
# 💭 Technical reflection: 
- if I use such a code:   most_often_key = [list(grades_number)[0]], the result is integer. When I want to get a list, I have to write such a code: most_often_key = [list(grades_number)[0]]
   
# 🔖 Tags / topics:
`TAG: dictionary | TAG: values | TAG: items`  
