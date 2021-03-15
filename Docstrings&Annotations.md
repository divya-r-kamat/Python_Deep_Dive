# Docscrings

We can document functions (and modules, classes etc) to return docstrings. If the first line in the function body is a string (not an assignment, not a comment, just a string (single quote, double quote , or triple quote - for multiline) by itself), it will be interpreted as a docstring

for eg:

	 def my_func(a):
		 '''documentation for my_func'''
		 return a
  
  
 Where are docstrings stored?
 
 In the functions __doc__ property
 
 ## Function Annotations (defines in PEP3107)
 
 Function annotations give us an additional way to document our functions, they can be any expression
 
	 def my_func(a: <expression> , b: <expression>) -> <expression>:
		pass
 
 	 def my_func(a : 'a string', b: 'a positive integer') -> 'a string':
	 	return a*b
		
	
