# Python Syntax Exercises
---

### count_up.py
```python
def convert_temp(unit_in, unit_out, temp):
    """Convert farenheit <-> celsius and return results.

    - unit_in: either "f" or "c" 
    - unit_out: either "f" or "c"
    - temp: temperature (in f or c, depending on unit_in)

    Return results of conversion, if any.

    If unit_in or unit_out are invalid, return "Invalid unit [UNIT_IN]".
    For example:

      convert_temp("c", "f", 0)  =>  32.0
      convert_temp("f", "c", 212) => 100.0
    """
    return (f"Invalid unit {unit_in}" if unit_in not in ('c', 'f') 
            else f"Invalid unit {unit_out}" if unit_out not in ('c', 'f')
            else temp if unit_in == unit_out 
            else temp * (9/5) + 32 if unit_in == 'c' 
            else (temp - 32) * (5/9))

    """    
    if unit_in != "f" and unit_in != "c":
        return f"Invalid unit {unit_in}"
    elif unit_out != "f" and unit_out != "c":
        return f"Invalid unit {unit_out}"
    elif unit_in == unit_out:
        return temp
    elif unit_in == "c":
        return temp * 1.8 + 32
    else:
        return (temp - 32) * 5/9

    if unit_in not in ['c', 'f'] or unit_out not in ['c', 'f']:
        return f"Invalid units {unit_in}, {unit_out}"    
    if unit_in == unit_out:
        return temp
    return temp * 1.8 + 32 if unit_in == 'c' else (temp - 32) * 5/9    
        """


print("c", "f", 0, convert_temp("c", "f", 0), "should be 32.0")
print("f", "c", 212, convert_temp("f", "c", 212), "should be 100.0")
print("z", "f", 32, convert_temp("z", "f", 32), "should be Invalid unit z")
print("c", "z", 32, convert_temp("c", "z", 32), "should be Invalid unit z")
print("f", "f", 75.5, convert_temp("f", "f", 75.5), "should be 75.5")
```
---
### in_range.py

```python
def in_range(nums, lowest, highest):
    """Print numbers inside range.

    - nums: list of numbers
    - lowest: lowest number to print
    - highest: highest number to print

    For example:

      in_range([10, 20, 30, 40], 15, 30)

    should print:

      20 fits
      30 fits
    """
    for num in nums:
        if lowest <= num <= highest:
            print(num)
    """
    if nums:
        num = nums.pop(0)
        if lowest <= num <= highest:
            print(num)
        in_range(nums, lowest, highest)

    result = map(lambda x: print(x), filter(lambda num: lowest <= num <= highest, nums))
    print(*result)

    {print(num) for num in nums if lowest <= num <= highest}

    result = [num for num in nums if lowest <= num <= highest]
    print(*result)
    
    result = filter(lambda num: lowest <= num <= highest, nums)
    print(*result)

    result = (num for num in nums if lowest <= num <= highest)
    print(*result)

    result = filter(lambda num: lowest <= num <= highest, nums)
    print(*map(str, result))

    i = 0
    while i < len(nums):
        if lowest <= nums[i] <= highest:
            print(nums[i])
        i += 1

    [print(num) for num in nums if lowest <= num <= highest]
    
    """

    # YOUR CODE HERE

in_range([10, 20, 30, 40, 50], 15, 30)            
```
---

### sum.py

```python
def sum_nums(nums):
    """Given list of numbers, return sum of those numbers.

    For example:
      sum_nums([1, 2, 3, 4])

    Should return (not print):
      10
    """  

    # Python has a built-in function `sum()` for this, but we don't
    # want you to use it. Please write this by hand.
    
    return_int = 0
    for num in nums:
        return_int+=num
    return return_int
    """
    if len(nums) == 0:
        return 0
    return nums[0] + sum_nums(nums[1:])
    
    index = 0
    sum = 0
    while(index != len(nums)):
        sum += nums[index]
        index += 1
    return sum


    return sum(nums)

    return sum(num for num in nums)
    return sum([num for num in nums])
    """


print("sum_nums returned", sum_nums([1, 2, 3, 4]))
```
---

### any7.py
```python
def sum_nums(nums):
    """Given list of numbers, return sum of those numbers.

    For example:
      sum_nums([1, 2, 3, 4])

    Should return (not print):
      10
    """  

    # Python has a built-in function `sum()` for this, but we don't
    # want you to use it. Please write this by hand.
    
    return_int = 0
    for num in nums:
        return_int+=num
    return return_int
    """
    if len(nums) == 0:
        return 0
    return nums[0] + sum_nums(nums[1:])
    
    index = 0
    sum = 0
    while(index != len(nums)):
        sum += nums[index]
        index += 1
    return sum


    return sum(nums)

    return sum(num for num in nums)
    return sum([num for num in nums])



    """


print("sum_nums returned", sum_nums([1, 2, 3, 4]))

```
---
### convert.py
```python
def convert_temp(unit_in, unit_out, temp):
    """Convert farenheit <-> celsius and return results.

    - unit_in: either "f" or "c" 
    - unit_out: either "f" or "c"
    - temp: temperature (in f or c, depending on unit_in)

    Return results of conversion, if any.

    If unit_in or unit_out are invalid, return "Invalid unit [UNIT_IN]".
    For example:

      convert_temp("c", "f", 0)  =>  32.0
      convert_temp("f", "c", 212) => 100.0
    """
    return (f"Invalid unit {unit_in}" if unit_in not in ('c', 'f') 
            else f"Invalid unit {unit_out}" if unit_out not in ('c', 'f')
            else temp if unit_in == unit_out 
            else temp * (9/5) + 32 if unit_in == 'c' 
            else (temp - 32) * (5/9))

    """    
    if unit_in != "f" and unit_in != "c":
        return f"Invalid unit {unit_in}"
    elif unit_out != "f" and unit_out != "c":
        return f"Invalid unit {unit_out}"
    elif unit_in == unit_out:
        return temp
    elif unit_in == "c":
        return temp * 1.8 + 32
    else:
        return (temp - 32) * 5/9

    if unit_in not in ['c', 'f'] or unit_out not in ['c', 'f']:
        return f"Invalid units {unit_in}, {unit_out}"    
    if unit_in == unit_out:
        return temp
    return temp * 1.8 + 32 if unit_in == 'c' else (temp - 32) * 5/9    
        """


print("c", "f", 0, convert_temp("c", "f", 0), "should be 32.0")
print("f", "c", 212, convert_temp("f", "c", 212), "should be 100.0")
print("z", "f", 32, convert_temp("z", "f", 32), "should be Invalid unit z")
print("c", "z", 32, convert_temp("c", "z", 32), "should be Invalid unit z")
print("f", "f", 75.5, convert_temp("f", "f", 75.5), "should be 75.5")
```
---
### words.py

```python
def print_upper_words(words, must_start_with={}):
    """Prints all words in the list in all uppercase."""
    for word in words:
        if len(must_start_with) == 0 \
        or any(word.upper().startswith(startwith.upper()) for startwith in must_start_with):
            print(word.upper())
"""
print_upper_words(["hello", "hey", "goodbye", "yo", "yes"],
                   must_start_with={"h", "y"})

print_upper_words(["hello", "hey", "goodbye", "yo", "yes"],
                   must_start_with={"y"})

print_upper_words(["hello", "hey", "goodbye", "yo", "yes"],
                   must_start_with={"h"})

print_upper_words(["hello", "hey", "goodbye", "yo", "yes"])
"""
print_upper_words(["hello", "hey", "goodbye", "yo", "yes"],
                   must_start_with={"h"})
```