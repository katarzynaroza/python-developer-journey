# 📝 Task - Create a function get_century() that:

Takes the integer year.
Returns the century for that year, where:

year = 0 should be processed as the first year of our era (and the first century);

1800 is still in the 18th century, but 1801 is in the 19th century (and so on).

<pre>
import math

def get_century(year: int) -> int:
    if year == 0:
        year = 1

    century = year / 100

    rounding = year % 100
    if rounding != 0:
        return int(math.ceil(century))
    return int(century)

print(get_century(100))  
</pre>
  
AFTER REFACTORING:  
<pre>
def get_century(year: int) -> int:
    if year == 0:
        year = 1

    return (year - 1) // 100 + 1

print(get_century(101))
</pre>

# 💭 Technical reflection: 
- Try to use theory that is given by Mate Academy to the task
- If I want to ask about code in Mate Academy chat, there is speccial function to give a code block.

# 🔖 Tags / topics:
`TAG: REFACTOR`  
