# 📝 Task - debugg a program

import pdb              <- here  
  
numbers = [1, "2", 3]  
my_sum = 0  
  
for number in numbers:  
    pdb.set_trace()   <- and continued  
    my_sum += number  
    print(my_sum)  
  
# 💭 Technical reflection: 
- it's just an example how to debugg, thanks PDB
- thanks pdb.set_trace() in main console, when i click play, i can see what will do the program nxt, i.e. my_sum += number and check, in with moment of making loop the program is.
  in that exemple, when I write in console "number" i will got the answer: 1,  when I write "my_sum": 0. When I will write "continue" the loop will make one more time. In next loop,
  when I write "number" i got '2', and when I write "type(number)" i can get to know it is str. Now i can write "c" to continue and i can see the program stop with error.

# 🔖 Tags / topics:
`TAG: PYTHON | TAG: DEBUGGING`  


