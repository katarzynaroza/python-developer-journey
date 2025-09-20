# 📝 Task - Developers have released an update for our app, and we need to check which of our robots haven't received it yet. Create a function get_outdated that:  
  
Takes a list of robots and an integer new_version.  
  
Returns a list of robot indices whose core_version is lower than new_version.
  
For example:  
<pre>
  robots = [
  { "core_version": 9 },
  { "core_version": 13 },
  { "core_version": 16 },
  { "core_version": 9 },
  { "core_version": 14 },
]

get_outdated(robots, 10) # [0, 3]
get_outdated(robots, 14) # [0, 1, 3]
get_outdated(robots, 8) # []
get_outdated(robots, 18) # [0, 1, 2, 3, 4]
</pre>  
💡 Use the built-in enumerate function to get the job done - details here.  
  
RESULT:  
<pre>
  def get_outdated(robots: list, new_version: int) -> list:
    outdated_list = []
    for index, robot in enumerate(robots):
        version = robot["core_version"]
        if version < new_version:
            outdated_list.append(index)
    return outdated_list
</pre>  

# 💭 Technical reflection: 
- Enumerate() function gives me index, 
- If I want to have full iteration, "return" can't be in loop,
- If I want to work on keys, I have to do that in this way: robot["core_version"]
- It is good to has some break in doing exercises - than it's easier to make them.
- here: robot["core_version"] I work on value of core version, not on the key. If I would like to work on the key, I should write in code just "core version" (without []).

# 🔖 Tags / topics:
`TAG: enumerate | TAG: dictionary`  
