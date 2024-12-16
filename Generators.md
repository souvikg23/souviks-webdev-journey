- new method to create [[iterators]] 
- uses a function called yield .
`def gen(n):`
	`for i in range(n) :`
		`yield i`
	`for i in gen(5)`
		`print (i)`

- when the function encounters "yield" it pauses, saves state and prints what yield wants
- [[Comprehension]]
- 