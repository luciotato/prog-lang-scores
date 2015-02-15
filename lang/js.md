"Javascript"
---------

IOP: GUI-glue for the browser

Readability
-----------

**RE-I: Readability Intended: 60/100**

* Pro: "js" has a low-count of reserved words (easy to memorize).

* Pro: JS literal object notation is great (see JSON).

*Error handling: GOOD*

* Pro: Exceptions (but no finally-clause)

**RE-NO: Readability Naturally occurring: 35/100**

* Con: When you include a callback as a closure, it affects readability.

* Con: The fact that "this" in the closure hasn't lexical scope also affects readability.

* Con: by using "{" as block separator, bad-formatted code leads to low-readability.

* Con: You can declare and call a function on the spot. The programmer reading the code believe is only a function declaration until he reach the end of the function and found "()" after the last "}".

**RE-LA: Resistance to Language-Abuse: 10/100**

* you can do almost anything bending js syntax.

Meta-Power:  40/100
---------

* JS do not have CT-tools built-in.

* JS uses duck-typing, so generic programming is the norm. Of course duck-typing affects performance.

* There is no "Compile-Time" for JS. Everything is declared dynamically. 

* You can declare new-functions at RT by using `eval`, but JS is not homoiconic, you can create valid js-code in a string, but it is not easy (as in LISP).

RT-Speed: 25/100 
----------------

Normal Javascript is 4 times slower than C.

Syntax-flexibility: 80/100
--------------------------

* almost everything is a expression
* highly composable expressions
* highly composable type and var declarations
* everything is dynamically created
