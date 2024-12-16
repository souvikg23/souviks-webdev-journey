- a function , that takes another function as argument and returns after change of some functionality.
- [[class decorators]] can also be made

- without altering the source code
-  can use [[wrapper]] functions to change functionality of fubctions.

`def decorator_fn(original_fn):`
	`def wrapper_fn(original_fn) :`
			`print ('wrapper did it)`
									     `return(original_fn())`
								`return (wrapper_fn)`

`@decorator_fn` 
`def display():`
	`print ('diplay fn ran')`

- [[chaining decortaors]] is also possible