# 📝 Task - Our database failed and some users lost the value of the first_name field. Fortunately, the first_name field, which is used for full_name, can be used to attach the first_name value.  
  
Create a restore_names function that:  
  
Takes a list of users.  
1. Assigns a first_name to users whose value is missing or invalid, based on the full_name field.  
2. If the first_name field is present but invalid (i.e., it doesn't match the full_name), update it with the correct value from the full_name.  
3. Doesn't return anything.  
  
For example:  
<pre>
users = [
  {
    "last_name": "Holy",
    "full_name": "Jack Holy",
  },
  {
    "last_name": "Adams",
    "full_name": "Mike Adams",
  },
  {
    "first_name": "WrongName",
    "last_name": "Potter",
    "full_name": "Harry Potter",
  },
]

restore_names(users)

# users == [
#   {
#     "first_name": "Jack",
#     "last_name": "Holy",
#     "full_name": "Jack Holy",
#   },
#   {
#     "first_name": "Mike",
#     "last_name": "Adams",
#     "full_name": "Mike Adams",
#   },
#   {
#     "first_name": "Harry",
#     "last_name": "Potter",
#     "full_name": "Harry Potter",
#   },
# ]
</pre>  
💡 Use in to check key ownership.  
  
  
RESULT:
<pre>
def restore_names(users: list) -> None:
    for user in users:
      full_name_list = user["full_name"].split()
      restored_first_name = full_name_list[0]
      if "first_name" not in user or user["first_name"] != restored_first_name:
          user["first_name"] = restored_first_name 
</pre>  
  
# 💭 Technical reflection: 
- First I writed:  "if first_name not in user or first_name != restored_first_name:" but I treated first_name like variable, but first_name is already a key. The keys have to be in quotation marks. Furthermore in this part: "first_name != restored_first_name:" I need to compare value of the key "first_name", that's why I had to exchange first_name to user["first_name"]. 

# 🔖 Tags / topics:
`TAG: split | TAG: dictionary`  
