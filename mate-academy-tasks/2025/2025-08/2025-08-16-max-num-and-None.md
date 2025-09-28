# 📝 Task - The find_max() function is supposed to find and return the largest number from a list of integers. However, it returns incorrect results due to an error:

def find_max(numbers):  
    max_num = None  
    for num in numbers:  
        if max_num < num:  
            max_num = num  
    return max_num  

Step-by-step task:  
Find and fix the error in the find_max() function.  
Make sure the function returns the correct results. Consider edge cases, such as empty lists—in these cases, None should be returned.
💡 Examine how the max_num variable is initialized and compared within the loop. Use PyCharm's debugging tools.

RESULT:  
<pre>
def find_max(numbers):  
    if not numbers:  
        return None  
    max_num = numbers[0]  
    for num in numbers:  
        if max_num < num:  
            max_num = num              
    return max_num
</pre>      
# 💭 Technical reflection:
- if not numbers:  
        return None  -> this part is helpful (when I want check if the list is empty)
- when I want to bugfix, i need to call the function at the end
- REMEMBER abut extreme cases, e.i. empty lists and and negative numbers.

# 📝 Task - The function should reverse a string (e.g., "Python" → "nohtyP"). For some reason, it only returns the first letter.

def reverse_string(text):  
----reversed_text = ""    
____for char in text:  
--------reversed_text = char  
----return reversed_text  
  
👉 Test it on "Ala has a cat".
  
  
RESULT:    
<pre>
def reverse_string(text):
    reversed_text = ""
    for i in range(len(text) - 1, -1, -1):
        reversed_text += text[i]
    return reversed_text
  
print(reverse_string("Ala ma kota"))  
</pre>

# 💭 Technical reflection: 


# 🔖 Tags / topics:
`TAG: bugfix | TAG: none | TAG: range`  
