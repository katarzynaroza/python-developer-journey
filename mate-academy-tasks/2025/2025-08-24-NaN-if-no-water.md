# 📝 Task - We're making lemonade for our friends. The number of servings we can make depends on the amount of sugar and water we have available. One serving requires 500 ml of water and 100 g of sugar.  
  <pre>
Create a function make_lemonade() that:

Takes two numbers, sugar_grams and water_liters.

Returns the number of servings we can make, where:

If we don't have water, we can't make lemonade—the function should return "NaN."
For example:

make_lemonade(500, 2) returns 4 servings because we only have two liters of water (4 x 500).
make_lemonade(600, 6) returns 6 servings because we only have 600 grams of sugar (6 * 100).
make_lemonade(300, 0) returns "NaN," because without water, we can't make lemonade.
💡 Use float("nan") for "NaN" and the built-in min function. For more information, see this geeksforgeeks article.
</pre>
<pre>
RESULT:
def make_lemonade(sugar_grams: float, water_liters: float) -> int:
    servings_sugar = sugar_grams // 100
    servings_water = (water_liters * 1000) // 500
        
    if water_liters == 0:
        return float("nan") # no water - no lemoniade    

    return min(servings_sugar, servings_water) # The number of possible servings depends on the ingredient that is less
</pre>

# 💭 Technical reflection: 
- First, condition  "if water_liters == 0:" I puted at the end of code, but in the way the code is now, it is quicker.
- I should also remeber, that in min() function I can put two or more variables, not only a name of list. If I don't creat additional list, that consist of servings_sugar and servings_water, the code is shorter and easier to read.
- It is good to think, wheter my code is clear and refactored enough.
- Comments should answear "why?", not "what happens in code?" and be as short as it's possible.

# 🔖 Tags / topics:
`TAG: NAN | TAG: MIN`  
