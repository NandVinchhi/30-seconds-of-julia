---
title: is_perfect
tags: math, beginner 
---

Checks if a number is perfect or not. 
A number is said to be perfect when the sum of its divisors excluding itself is equal to that number.

use of '%' to check for divisiblity. 
checks if sum of divisors is equal to the number.

```jl
function is_perfect(n)
	s = 0
	for i = 1:Int(floor(n/2))
		if n % i == 0
			s += i 
		end
	end
	if s == n
		return true
	else
		return false 
	end
end
```

```jl
is_perfect(10) # false
is_perfect(28) # true
```
