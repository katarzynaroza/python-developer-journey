# 📝 Task - Counting grades above the threshold  
  
Write a function count_above_threshold that:  
- takes the dictionary class_register and the number threshold,  
- returns the number of students whose grade is greater than or equal to threshold.

RESULT:
<pre>
def count_above_threshold(class_register: dict, threshold: int) -> int:
    counter = int()
    list_of_values = list(class_register.values())
    for grade in list_of_values:
        if grade >= threshold:
            counter += 1
    return counter

class_register = {"Anna": 5, "Milena": 3, "Zuzanna": 5, "Aleksandra": 4}
print(count_above_threshold(class_register, threshold = 4)) # 3
</pre>
# 💭 Technical reflection: 
- when I use values() function in for loop (I mean this code:  "for grade in list_of_values:"), I don't have to work only on "value" word, I can also use "grade" word.

# 🔖 Tags / topics:
`TAG: values | TAG: dictionary`  
