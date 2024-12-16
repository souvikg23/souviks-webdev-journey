`x = {key : value}`

`print(student[key])`


- to stop from using a key that doesn't exist , we can use  get method
`print(student.get(key))`

when used this way,
- returns "None" by default if the key is not found.
- else, you can customize thye messege returned for not finding as the second argument in get.
`print(student.get(key,'Not there'))`

- deleting a pair:
`del student[key]`
OR
`x = student.pop('age')`

- to print key-value pairs use .items( :)
for key,value in student.items():
	print(key,value)