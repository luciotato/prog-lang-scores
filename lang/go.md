"Go-lang"
---------

IOP: Highly-scalable services (google level)

Readability
-----------

**RE-I: Readability Intended: 65/100**

"go-lang" has a low-count of reserved words (easy to memorize).

**Line read: MEDIUM**

function declaration with a receiver section, plus tuple-return values
makes methods declaration confusing (three sections enclosed in parenthesis)

**Readability and Error handling:**

* Con: No Exceptions 

Lacking exceptions, good golang code has error-handling code after/with each important function call, cluttering the normal flow, hindering readability (readability defined as how easy is to understand what the code is doing)

All important functions return a tuple (result,err). In good golang code the line starts with "if" (to check the error). This hinders readability.


**RE-NO: Readability Naturally occurring: 60/100**

* golang uses "{" as block separator, but it is not optional (as in C). 

* gofmt fixes bad-formatted code.

**RE-LA: Resistance to Language-Abuse: ??/100**

Meta-Power:  20/100
---------

* golang do not have a preprocessor nor templates (they are reluctant to re-make C++'s mistakes).

* There is an ad-hoc code generator based on comments: go generate. (http://blog.golang.org/generate)

RT-Speed: 50/100 
----------------

Normal golang is 2 times slower than C.

Syntax-flexibility: ??/100
--------------------------

* almost everything is an expression?
* highly composable expressions
* highly composable type and var declarations
