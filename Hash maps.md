1) create a list
```
```python
prevMap = {}  # val -> index
```

3) define a key variable : can use [[enumerate]] to rotate through the array/list
```
```python
 for i, n in enumerate(nums):
            diff = target - n
					            if diff in prevMap:
	        return  ![[Pasted image 20241023235734.png]][prevMap[diff], i]
            prevMap[n] = i
```

5) assign those keys to values