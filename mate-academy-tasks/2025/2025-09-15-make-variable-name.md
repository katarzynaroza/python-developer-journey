# 📝 Task - Programmers love long variable names. To turn a regular sentence into a variable name, we need to replace all spaces with underscores.  
Create a function make_variable_name that:  
  
Takes a string words and an integer number_of_words.  
  
Returns a variable name composed of the first number_of_words of words—separated by underscores.  
  
For example:  
<pre>
make_variable_name("x", 1) # "x"
make_variable_name("a plus b problem", 3) # "a_plus_b"
make_variable_name("my favorite variable name is x", 3) # "my_favorite_variable"
</pre>  
RESULT:
<pre>
def make_variable_name(words: str, number_of_words: int) -> str:
    words_list = words.split()
    variable_list = []
    for i in range(number_of_words):
        variable_list.append(words_list[i])

    variable_name = "_".join(variable_list)
    return variable_name
</pre>  
BUT AFTER REFACTORISATION:  
<pre>
def make_variable_name(words: str, number_of_words: int) -> str:
    words_list = words.split()
    variable_name = "_".join(words_list[0:number_of_words])
    return variable_name

print(make_variable_name("a plus b problem", 3)) # a_plus_b
</pre>    
OR:  
<pre>
def make_variable_name(words: str, number_of_words: int) -> str:
    variable_name = "_".join(words.split()[0:number_of_words])
    return variable_name

print(make_variable_name("a plus b problem", 3)) # a_plus_b
</pre>

# 💭 Technical reflection: 
- it is good to think about refactorisation, but in the way the code still is readable  
- maybe next time I will give some explanatations in code, by "#"
- I tried to delate the last line of function, i.e. "return variable_name", but in console I saw "None". It means, that even if I print the function, the code of function have to return sth.

# 🔖 Tags / topics:
`TAG: split | TAG: join | TAG: refactorisation` 
