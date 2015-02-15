"C++ lang"
---------

IOP: Systems programming, OOP programming

CT-Tools:
* C++ preprocessor: #include, #define, #ifdef, ...
* C++ templates: code-generation by templates


CT-Power:  30/100
---------

* Compile-time tool-1 for C++ is the preprocessor. The language of preprocessor directives is only weakly related to the grammar. The preprocessor is a "text-processor", and a low-power one.

References:
http://www.boost.org/doc/libs/1_57_0/libs/preprocessor/doc/topics/problems.html

* Compile-time tool-2 is "C++ Templates". Templates can become a nightmare really fast. 

 
RT-Speed: 95/100 
-------------

"C++" is almost "C" plus classes. You pay with some performance when you use virtual method dispatch.

Readability
-----------

**RE-I**: Readability Intended: 70/100

"C" has a low-count of reserved words (easy to memorize).

**Line read: GOOD**

* C++ generic statement form is:
  - "type name [=expression]" (to declare a var)
  - "type name()" (to declare a function)
  - "name([expression,...])" (to make a function call)

Note: Here the opening parenthesis acts as a postfix sigil to separate function names from variable names.

  - "x = expression" destructive assignment

  Other c statements are easily recognized because they *start with* their reserver word: "if","for","while","return",etc.

**Pro**: C-lang "&" sigil meaninig "address-of" can be used also in function parameter definition meaning: "give me a pointer, but I'll treat it internally as a value"

**Error handling: BETTER**

C++ adds exceptions. Error-handling can be moved to `catch` blocks, this eases readability (readability defined as how easy is to understand what the code is doing)

**Con:** no `finally` clause.

**RE-NO**: Readability Naturally occurring: 40/100

* In real world examples, heavy use of #define and templates makes C++ code harder to read.
* by using "{" as block separator, bad-formatted code leads to low-readability.
* Unidimensional source and the "{" being optional, make some [dangerous bugs possible]
(http://luciotato.svbtle.com/adding-a-new-dimension-to-source-code). 

**RE-LA**: Resistance to Language-Abuse: 20/100

Given the abuse of the c-preprocessor on the wild, this score should be 10, but being the preprocessor such a lousy CT-tool, it acts as a natural remedy against CT-power abuse. 

* High syntax-flexibility (assignment is an expression) also hurt readability. `if (a=b) printf("strange, they're equals")` is a common beginner bug.

* Operator overloading hurt readability. `a+b` could be anything.

Syntax-flexibility: 70/100
--------------------------

* almost everything is a expression
* highly composable expressions
* highly composable type and var declarations
* operator overloading
* templates
