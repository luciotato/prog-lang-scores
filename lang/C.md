"C-lang"
--------

IOP: Systems programming

Readability:  
-----------

**RE-I: Readability Intended: 50/100**

"C" was designed as a higher-level than assembly language. Today is C is the portable assembler.

"C" has a low-count of reserved words (easy to memorize).

**Line read: GOOD**

* C's generic statement form is:
  - "type name" (to declare a var)
  - "type name()" (to declare a function)
  - "name()" (to make a function call)

Here the opening parenthesis acts as a postfix sigil to separate function names from variable names.

**Readability and Error handling:**

Lacking exceptions, good C code has error-handling code after each important function call, cluttering the normal flow, hindering readability (readability defined as how easy is to understand what the code is doing)

**RE-NO: Readability Naturally occurring: 40/100**

* In real world examples, heavy use of #define makes C code harder to read.
* by using "{" as block separator, bad-formatted code leads to low-readability.
* Unidimensional source and the "{" being optional, make some [dangerous bugs possible](https://blog.codecentric.de/en/2014/02/curly-braces/) (http://luciotato.svbtle.com/adding-a-new-dimension-to-source-code). 

**RE-LA: Resistance to Language-Abuse: 20/100**

Given the abuse of the c-preprocessor on the wild, this score should be 10, but being the preprocessor such a lousy CT-tool, it acts as a natural remedy against CT-power abuse. 

High syntax-flexibility also hurt readability. `if (a=b) printf("strange, they're equals")` is a common bug. When used intentionally, (assignment inside an if expression) is at least confusing for the reader. 


Meta-Power:  35/100
-----------

CT-Tools: C-lang preprocessor: #include, #define, #ifdef, ...

* Compile-time code for C-lang is the C-preprocessor. The language of preprocessor directives is only weakly related to the grammar of C. The C-preprocessor is a "text-processor", and a low-powered one.

References:
http://www.boost.org/doc/libs/1_57_0/libs/preprocessor/doc/topics/problems.html

 
RT-Speed: 100/100 
-----------------

"C-lang" is the unit of measure for performance. All other langs will be measured against it.


Syntax-flexibility: 70/100
----------------------

* almost everything is an expression
* highly composable expressions
* highly composable type and var declarations

