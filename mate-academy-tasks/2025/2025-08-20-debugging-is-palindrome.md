# 📝 Task - The function is available to check whether a given string is a palindrome (e.g. "kayak" → True). Now, however, always pay attention to False.  
  
RESULT:  
def palindrome(s):  
____i = 0  
____while i <= len(s) / 2:  
________if s[i] != s[-i - 1]:  
____________return False  
________i += 1  
____return True  
    
print(palindrome("krzak"))  
  
or    
  
def palindrome(s):  
____i = 0  
____while i <= len(s) - 1:  
________if s[i] != s[-i - 1]:  
____________return False  
________i += 1  
____return True  

# 💭 Technical reflection: 
- I asked in english in google: "is palindrom function" - I found the code on stack overflow

# 🔖 Tags / topics:
`TAG: PYTHON`  


