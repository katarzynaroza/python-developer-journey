# 📝 Write a group_by_threshold function that:  
  
- takes the class_register dictionary and the threshold value,  
- returns a dictionary with two keys: "pass" and "fail."  
- "Pass" is where you put students whose grade is ≥ threshold,  
- "Fail" is where you put those whose grade is below the threshold.

RESULT:
<pre>
def group_by_threshold(class_register: dict, threshold: int) -> dict:

    result_register = {}
    result_register["pass"] = []
    result_register["fail"] = []

    if not class_register:
        return result_register

    for name, grade in class_register.items():
        if grade >= threshold:
            result_register["pass"].append(name)
        else:
            result_register["fail"].append(name)
    return result_register


class_register = {"Anna": 5, "Milena": 3, "Zuzanna": 5, "Aleksandra": 4}
print(group_by_threshold(class_register, threshold = 4))
</pre>
  
# 💭 Technical reflection: 
- else means: "everything else that wasn't included in if/elif".
- if → mandatory condition.
- elif → mandatory condition.
- else → no condition, only "otherwise".
- a value in a dictionary can also be a list.

# 🔖 Tags / topics:
`TAG: dictionary | TAG: else | TAG: elif`  
