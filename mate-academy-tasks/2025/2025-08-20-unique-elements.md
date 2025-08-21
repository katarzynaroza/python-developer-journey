# 📝 Task - The function was supposed to return a list of unique elements, but now it returns an empty list. def unique_elements(numbers): result = [] for num in numbers: if num not in result: result = [num] return result 👉 Check: unique_elements([1, 2, 2, 3, 4, 4])

RESULT:   
def unique_elements(numbers): 
<pre>
    result = []
    for num in numbers:
        if num not in result:
            result.append(num)
    return result  </pre>
  
print(unique_elements([1, 2, 2, 3, 4, 4]))  

the function will return [1, 2, 3, 4]

# 💭 Technical reflection: 
- it was easy debugging task, but the below part ist interesting, mayby helpful:  
for num in numbers:  
        if num not in result:  

# 🔖 Tags / topics:
`TAG: PYTHON`  
