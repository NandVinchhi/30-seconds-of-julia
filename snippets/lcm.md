---
title: lcm
tags: math,intermediate
---

This function calculates the LCM of two integers. The LCM is obtained by dividing the product of the two numbers by their GCD. 

```jl
function lcm(a, b)
  l = a > b ? a : b
  HCF = 1
  for i = 2:Int(floor(l/2))
    if a % i == 0 && b % i == 0 && i > HCF
      HCF = i 
    end
  end
  return (a * b)/HCF
end
```

```jl
lcm(4, 8) # 8.0
lcm(9, 12) # 36.0
lcm(296, 84) # 6216.0
```
