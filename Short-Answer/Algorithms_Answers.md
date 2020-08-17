#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) The loop checks if a is less than n cubed while adding n squared to a with each iteration of the loop. Since it takes n times to iterate through the loop the runtime is O(n)

b) There's two loops: The for loop which runs n times and the inner loop which compares j and n. Every time the inner loop runs, j doubles so the the breakpoints of when the inner loop would stop are on exponents of 2. The runtime is O(n*log2(n)). 

c) This is a recursive function that runs itself when bunnies is at 0. Every time the function recurses bunnies decreases by 1. The runtime is O(bunnies)

## Exercise II

I'll go with a binary search. Divide the floors in half and stick with the middle floor. If the egg breaks, discard the upper floors. The middle floor would be the highest floor as a possibility for f. Next, divide the remaining floors below in half, moving to the middle floor. If the egg doesn't break discard the floors below and consider the floors above. Keep repeating this function of dividing remaining floors in half until the lowest floor where the egg breaks and assign that to f. This solution will have a runtime complexity of O(log(n)).

Example:

My building is 100 stories tall and eggs don't break at floors below floor 20. 

Floors 1-100, mid = 51, break
Floors 1-50, mid = 26, break
Floors 1-25, mid = 13, safe
Floors 13-25, mid = 19, safe
Floors 19-25, mid = 22, break
Floors 19-21, mid = 20, safe
Floors 20-21, mid = 21, break From here. The search would know that floor 20 is a safe floor, and that floor 21 broke the egg. Floor 20 is the floor I'm looking for.