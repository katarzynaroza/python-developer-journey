# 📝 Task - Imagine we're running a store and storing a list of products in stock as a dictionary, where keys are product names and values ​​are their counts. We want to be able to quickly check product availability and quantity without triggering an error if a product is out of stock.  
  
Create a check_item_stock function that:  
Takes a dictionary and the product name, item_name, to check.  
Uses the get method to obtain the product's stock count.  
  
If the product is listed and its stock count is greater than zero, it returns True. Otherwise, it returns False.  
  
For example:  
<pre>
inventory = {"apples": 30, "bananas": 45}
item_name = "oranges"

check_item_stock(inventory, item_name) # False
</pre>  
RESULT:  
<pre>
def check_item_stock(inventory: dict, item_name: str) -> bool:
    item_value = inventory.get(item_name, 0)
    return item_value > 0
</pre>
# 💭 Technical reflection: 
- At the beginning I used "for" loop, but here it's not nesesery.  
- The get method checks whether a key exists in the dictionary. If the key (item_name) is in the inventory, it returns its value; if not, it returns a default value (e.g., 0). This eliminates the need to separately check for the key's existence.  
- To check if a key (e.g. product name) is in the dictionary, you use: "if item_name in inventory:" (item_name is variable with key inside for exapmple item_name = "orange").  
- To retrieve a value (e.g. product quantity), you use: quantity = inventory[item_name] # WARNING: error if key is not present!  
- But to retrieve a value it's safer to use: quantity = inventory.get(item_name, 0)  # there is no error, if key doesn't exist.
 

# 🔖 Tags / topics:
`TAG: get | TAG: dictionary`  
