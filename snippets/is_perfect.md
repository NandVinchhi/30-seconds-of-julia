---
title: is_perfect
tags: math, beginner 
---

Checks if a number is perfect or not. 
A number is said to be perfect when the sum of its divisors excluding itself is equal to that number.

Use of '%' to check for divisiblity. 
Checks if sum of divisors is equal to the number.

```jl
function is_perfect(n)
	s = 0
	for i = 1:Int(floor(n/2))
		n % i == 0 ? s += i : s += 0
	end
	return s == n ? true : false
end
```

```jl
is_perfect(10) # false
is_perfect(28) # true
```
