# 📝 Task - We're working on a "Yes or No" game. Help us by creating a yes_or_no function that:

1. Returns "Yes" if the argument is True, otherwise "No."  
2. Returns "No" if word_request is "no."  
💡 "no" is a special case and takes precedence over normal conversion to bool().  

For example:  
<pre>
yes_or_no("yes") == "Yes"
yes_or_no("no") == "No"
yes_or_no(1) == "Yes"
yes_or_no(0) == "No"
yes_or_no([]) == "No"
yes_or_no([""]) == "Yes" 
yes_or_no("") == "No"
</pre>  
RESULT:  
<pre>
def yes_or_no(word_request: Union[str, int, list, None]) -> str:
    if word_request == "no":
        return "No"
    if bool(word_request) == True:
        return "Yes"
    else:
        return "No"
</pre>  
OR:  
<pre>
from typing import Any
def yes_or_no(word_request: Any) -> str:
    
    if isinstance(word_request, str):  # Check if argument is string (that is needed to check "no" argument)
        if word_request.lower().strip() == "no":
            return "No"
    return "Yes" if bool(word_request) else "No"
</pre>

# 💭 Technical reflection: 
- if word_request = "no": — Python won't run. This is a SyntaxError, because = is an assignment, and if requires a logical condition (==).
- for None, the result of bool(None) is False.
- Union for argument helps in giving different types of datas.
- Thanks any I can use whole types of arguments (I have to import "from typing import Any").
- it is interesting to use to "if" in one line: return "Yes" if bool(word_request) else "No".

# 🔖 Tags / topics:
`TAG: None | TAG: Union | TAG: Any`  
