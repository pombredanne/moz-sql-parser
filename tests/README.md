Moz SQL Parser Tests
====================

The parser is not complete! Please help by adding a test, and then altering the grammar to pass that test.

## Running Tests

	git clone https://github.com/mozilla/moz-sql-parser.git
	pip install -r requirements.txt
	set PYTHONPATH=.	
	python.exe -m unittest tests.test_simple

### Debugging Suggestions

* Once you have written a failing test, you can `DEBUG=True` in the 
`sql_parser.py` to print out a trace of matching attempts. 
* If you added more `ParserElement`s, you may want to add `.setDebug(DEBUG)` 
to each, so they print out thier matching attempts too.
* Even though you can use Python strings for literals, they will not be
attempted in all cases; wrap as a `Literal` or `Keyword`.  This problem 
is known to lurk while matching `infixNotation`. 
* Feel free to leave in rulers, if you use them

 

