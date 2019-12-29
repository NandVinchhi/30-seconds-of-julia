---
title: is_palindrome
tags: string, beginner
---

This function returns a boolean value based on whether the input string is a palindrome or not.

checks if the (i)th index is equal to the (n - i + 1)th index, where n is the length of the string.

```jl
function is_palindrome(s)
	str = lowercase(s)
	len = length(str)
	for i = 1:Int(floor((len/2)))
		if str[i] != str[len - i + 1]
			return false
		end
	end
	return true
end
```

```jl
is_palindrome("abcdefg") #false
is_palindrome("abcdcba") #true
```
