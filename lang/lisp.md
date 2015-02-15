"LISP"
---------

IOP: Recursive Symbolic List processing

http://swizec.com/blog/the-birth-of-lisp-a-summary-of-john-mccarthys-original-paper/swizec/5075

http://www.paulgraham.com/rootsoflisp.html

Readability
-----------

**RE-I: Readability Intended: 30/100**

LISP is also known as "Lots of Irritating Superfluous Parentheses".
A Lisp expression must be read inside-out to understand what the code is doing. A deep-nested expression is a nightmare. LISP is beautiful but not readable.

**RE-NO: Readability Naturally occurring: 20/100**


**RE-LA: Resistance to Language-Abuse: 5/100**

You can do almost anything to LISP in LISP itself.

Meta-Power:  100/100
---------

CT-Tools:

* LISP Itself. You have the entire language power at CT for code generation.

* LISP uses duck-typing, so generic programming is the norm. Of course duck-typing affects performance.


RT-Speed: 30/100 
-------------

Lisp SCBL is 3 times slower than C.

http://benchmarksgame.alioth.debian.org/u64q/compare.php?lang=sbcl&lang2=gcc

Syntax-flexibility: 100/100
--------------------------

* everything is an s-expression
* highly composable expressions
* everything is dynamically created
