"Javascript"
---------

IOP: GUI-glue for the browser

CT-Tools:

* JS do not have CT-tools built-in.

* JS uses duck-typing, so generic programming is the norm. Of course duck-typing affects performance.


CT-Power:  40/100
---------

* There is no "Compile-Time" for JS. Everything is declared dynamically. 

* You can declare new-functions at RT by using `eval`, but JS is not homoiconic, you can create valid js-code in a string, but it is not idiomatic (as in LISP).

RT-Speed: 25/100 
-------------

Normal Javascript is 4 times slower than C.

Readability
-----------

**RE-I**: Readability Intended: 60/100

"js" has a low-count of reserved words (easy to memorize).

**Line read: GOOD**

**Error handling: GOOD**

* Exceptions (but no finally-clause)

**RE-NO**: Readability Naturally occurring: 50/100

* by using "{" as block separator, bad-formatted code leads to low-readability.

**RE-LA**: Resistance to Language-Abuse: 10/100

Syntax-flexibility: 80/100
--------------------------

* almost everything is a expression
* highly composable expressions
* highly composable type and var declarations
* everything is dynamically created
