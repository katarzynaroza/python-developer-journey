# 📝 Task - Create a function multiply_numbers that:  
  
Returns the result of multiplying a by b if the function receives both numbers.  
Returns either a or b unchanged if it receives only one number.  
The function can receive any number of positional/named arguments, but should ignore all.  
If nothing is passed to the function, return 1.  
Examples:  
<pre>
multiply_numbers() == 1
multiply_numbers(2, 3) == 6
multiply_numbers(b=5) == 5 
multiply_numbers(4, 3, "string", []) == 12
multiply_numbers(1, 3, "string", k=22) == 3
</pre>

RESULT:  
<pre>
def multiply_numbers(a: int = None, b: int = None, *args, **kwargs):

    if a is not None and b is not None:
        return a * b
    if a is None and b is None:
        return 1
    if a is None:
        return b
    else:
        return a
</pre>

# 💭 Technical reflection: 
- It is interesting, that in if condition I can use "if sth is not None and sth is None".

# 🔖 Tags / topics:
`TAG: args | TAG: kwargs`  
