# 📝 Task - Create a function weekday_order that:  
  
1. Takes a string representing the day of the week (e.g., "Monday").  
2. Returns a number representing the order of the day of the week (0 for "Monday," 1 for "Tuesday," up to 6 for "Sunday").  
  
Then create a function sort_weekdays that:  
  
1. Takes a list of weekdays in random order.  
2. Returns an ordered list of days from "Monday" to "Sunday," where:  
  
The function weekday_order must be passed to the function sorted as the sort key, based on which the weekdays will be sorted.  
  
For example:  
<pre>
sort_weekdays(["Monday"]) # ["Monday"]sort_weekdays(["Saturday", "Wednesday"
sort_weekdays(["Monday"]) # ["Monday"]
sort_weekdays(["Saturday", "Wednesday"]) # ["Wednesday", "Saturday"]
</pre>  
THE ANSWER:  
<pre>
def weekday_order(weekday: str) -> int:
    list_of_days = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]

    if weekday not in list_of_days:
        raise ValueError("Wrong weekday")
    return list_of_days.index(weekday)

def sort_weekdays(weekdays: list) -> list:
    sorted_weekdays = sorted(weekdays, key = weekday_order)
    return sorted_weekdays
</pre>

# 💭 Technical reflection: 
- raise ValueError("Wrong weekday") belong to Python exceptions, i.e. if there is some error, in this case in console I will see what to do, to the user will see that an error has occurred, but with a message that will direct him to correct the error.
- Python has predetermined exceptions, I can't rather make a new one. Thanks this exceptions in tasks, where the result has to be integer, I can make exception to tell the user, what is wrong.
- If I am not sure, what to do, it's good to check the method of lists or strings, or whatever I use.

# 🔖 Tags / topics:
`TAG: exception`  
