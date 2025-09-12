# 📝 Task - Our friend runs a hotel. Because his reservation form field, "number of guests," accepts strings, his managers often have to manually retrieve the number of guests:
<pre>
Room for 4 guests, please
Exactly 2 people
Meh, I'll be alone
</pre>
We can enhance the calculate_guests() function to automatically extract numbers from the guests_input string. If the function doesn't find a number or detects 0, it should return "not a number."  
  
Satisfy the following conditions:  
  
Extract only integers from the string; ignore decimals.  
If the string contains two integers, extract the first one.  
For example:
<pre> 
calculate_guests("I think 5 guests") # 5
calculate_guests("Big company of 15 dudes") # 15
calculate_guests("5") # 5
calculate_guests("alone") # "not a number"
calculate_guests("0") # "not a number"
calculate_guests("Hello, 9.75 people") # 9
calculate_guests("There will be 7 or 9 guys") # 7
calculate_guests("hello cat walks on my keyboard ksadjfhskaj12.34kasdfhsjk") # 12
</pre>

THE ANSWER:
<pre>
  def calculate_guests(guests_input: str) -> int | str:
    number = ""
    if guests_input == "0":
        return "not a number"
    for char in guests_input:
        if char.isnumeric():
            number += char
        elif len(number) > 0:
            break
    if len(number) == 0:
        return "not a number"
    return int(number)
</pre>

# 💭 Technical reflection: 
- It is usefull to get help from pycharm debuger.
- Elif mean: "otherwise and".

# 🔖 Tags / topics:
`TAG: isnumeric`  
