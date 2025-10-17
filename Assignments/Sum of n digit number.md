# Sum of n digits in a number

[image]

Steps: 
- We have to create a variable that can take the number
- We have to convert the number in to string: Then it will be able to access its each digits.- 
- Next step is to make a list with each digit of converted numbers.
- We will use list comprehesions for doing thi
- Step 2,3  will be done in list (ste 4)

First we will try with a small practice like 1234. Then we will make the code for any numbers like : n numbers.

print(f"Sum for {num} =", digit_sum)
## 1. Simple Solution
```python
num = 1234
print(sum([int(a) for a in str(num)]))
```
OUTPUT:	`10`

## 2. Adveced Solution

```python
num = input("Enter a number: ")
print(sum([int(a) for a in str(num)]))  # str() can remove as input already collects number as string
```
OUT:	i.e., 123 = `6`, 1234 = `10`, 4896 = `27`


**Lets try with different approach:**

If you think to make the code like the steps we discussed, it will give wrong answers:
```python
IN:	num = 1234
con_str = str(num)
con_int = int(con_str)
result = [con_int for a in con_str]
print(sum(result))
```
OUT:	4936