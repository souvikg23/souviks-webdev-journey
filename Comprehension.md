- another way for generator

`x = (i for i in range(10))`

`for j in x:`
	`print(j)`

- interesting , same used for [[lists]] and [[dictionary]] comprehension
  
  : ([[list comprehension]])
  ([[Dictionary Comprehention]])
- reminds me of [[lambda functions]]
- if used with ( ) as in the example the out put is generator object
- if used with { } output = set 
- if used with { } with key val pair, out put is dictionary 
`{x:2*x for x in range(3)}`
