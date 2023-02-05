 # Code 
 ```.py
 def to_roman(num:int):
    out = ""
    roman = {100: 'C', 90: 'XC', 50: 'L', 40: 'XL', 10: 'X', 9: 'IX', 5: 'V', 4: 'IV', 1: 'I'}
    if num < 1 or num > 100:
        raise ValueError("Number must be between 1 and 100")
    if not isinstance(num, int):
        raise TypeError("Number must be an integer")
    while num > 0:
        for i in roman.keys():
            if num >= i:
                out += roman[i]
                num -= i
                break
    return out
```
## Test
![]()
