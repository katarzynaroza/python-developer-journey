# 📝 Task - Our friend runs a car rental company. Customers enter the number of days they want to rent a car for in the days_input field, but the entries vary widely:
<pre> 
"I need the car for 3 days"
"Just 1 day"
"Maybe 0 days?"
"Two weeks (14 days)"
</pre>  
Your task is to write a function, calculate_days(days_input), that:  
  
Extracts only integers from a string (ignoring decimals).  
  
If it finds more than one number, it should return the smallest one (the client sometimes writes 14 and an additional 2, but we're interested in the smaller value – we assume it's the number of days).  
  
If it doesn't find any numbers, or if the number is 0, it returns the message "invalid rental."  

Examples:
<pre>
calculate_days("I need the car for 3 days")      # 3
calculate_days("Just 1 day")                     # 1
calculate_days("Maybe 0 days?")                  # "invalid rental"
calculate_days("Two weeks (14 days)")            # 14
calculate_days("14 days, maybe only 2 actually

</pre>  
THE ANSWER:  
<pre>
  def calculate_days(days_input):
    number = ""
    list_of_numbers = []

    # here I check the input wheter is numeric
    for char in days_input:
        if char.isnumeric():
            number += char
        elif len(number) > 0:
            list_of_numbers.append(int(number))
            number = ""

    # here I give instruction in case, the last char is numeric
    if len(number) > 0:
        list_of_numbers.append(int(number))

    # here I give instruction in case the list is empty
    if not list_of_numbers:
        return "invalid rental"

    # here I give the instruction in case, one of the item of list ist 0
    if 0 in list_of_numbers:
        return "invalid rental"

    if len(list_of_numbers) >= 2:
            return min(list_of_numbers)
    return list_of_numbers[0]


print(calculate_days("14 days, maybe only 2 actually"))
</pre>
  
# 💭 Technical reflection: 
- not always I need to use a loops, for example here:
<pre>
      if len(list_of_numbers) >= 2:
            return min(list_of_numbers)
    return list_of_numbers[0]
</pre>

# 🔖 Tags / topics:
`TAG: isnumeric`  
