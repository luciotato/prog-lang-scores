Meta-Programming
================

Most programming languages allows you to write code on two levels: 

* Run-Time code: "RT-code" aka "ground level code", i.e. the code solving the actual problem you're focusing on.

* Compile-Time code: "CT-code" aka "meta-programming", "level 1 code", e.g. macros, preprocessor directives, code generation, templates, generic programming.

This two levels have **completely different** *domains*. This is a fundamental distinction, and something you must be aware-of in order to avoid destroying your productivity.

Level Domain
------------

###Ground Level

Run-time programming (RT-code) **domain** is whatever problem you are working on. On RT-level, you write code to solve the problem you are working on. 

RT-code *primary domain* is normally the "**intended original purpose**" of the language you're using, e.g.: general purpose, operating systems, symbolic list processing, formula translation, business processes, database query, database procedures, GUI-glue, etc.

###Level 1 (Meta)

**Compile-time programming (CT-code) domain is the RT-code itself**. You work with blocks of RT-code. You can operate on them, write CT-code to generate RT-code, or generate RT-code by template. 

CT-code is meta-programming, you write code to generate code to solve the problem you're working on.  

Measuring Programming Languages
--------
In this github repository I will collect a list of programming languages with:

* Their "intended original purpose" ("IOP")

* The power-level of their meta-programming tools ("CT-Power")

* the RT-speed (measured against C-lang)

* a Readability score

* a Syntax-flexibility score


All values are measured in a 0 to 100 scale. Where 0 is no-power and 100 is full-power.

###RT-speed

RT-speed is measured in a scale from 0 to 100, where 100 is *C-lang* speed. Example: RT-speed=50 means RT-code runs at half the speed of a similar algorithm coded in C-lang.

Speed is measured for multi-core 64-bit processors.

###Readability

Readability is tricky to measure. The idea is to evaluate how easy is to understand *"what the f#&! the code is doing"* by just reading it. The *"canonical subject"* reading the code is a programmer with **basic** experience on the language.

There are three measures of readability: 

 **1) RE-I**: Readability "as intended". When you use the language as designed *without abusing* syntax constructions and meta-programming tools.

 **2) RE-NO**: Readability "naturally occurring". Real-word examples of language usage. It measures how readable the code really is *when you're solving real-world problems* (instead of writing "hello world" examples). i.e.: The linux kernel is a good example of RE-NO for C-lang.
   
 **3) RE-LA**: "Resistance to language abusing". Measures how resistant the language is when a "clever" programmer decides to "use to the fullest" (abuse) syntax constructions and meta-programming tools. Low RE-LA (low resistance) means a "clever" programmer can abuse the language into unreadability, High RE-LA means the language fights back, or has less flexibility. 

Normally there's a **trade-off** between **readability** and **CT-power + syntax-flexibility**.

###Syntax-flexibility

Syntax-flexibility score intends to measure how "flexible" are the language syntax constructs. 
For example, C-lang’s type definition syntax is composable and highly-flexible. You can write: `void (*signal(int, void (*fp)(int)))(int);` which means: *"signal is a function passing an int and a pointer to a function passing an int returning nothing, returning a pointer to a function passing an int returning nothing"*. (http://c-faq.com/decl/spiral.anderson.html)

The example above shows C's high syntax-flexibility leading to low readability. (for the "canonical programmer") (http://blog.golang.org/gos-declaration-syntax)

Other indicators of high syntax flexibility are: "everything is a function", "closures", "homoiconicity" and "there is more than one way to do it" (http://ceronman.com/2012/09/17/coffeescript-less-typing-bad-readability)
 
The problem is that **high syntax flexibility normally leads to low readability (RE-NO and RE-LA mostly)**.


Hackers Collaboration
-----------
The language list in this repo is ridiculously short and the scores are blatantly arbitrary.
Pull requests are welcomed, to add languages, to add information, to correct mistakes. 

Try to remain objective and do not to stretch definitions to benefit one language or another.

Language Table
---------------

Click on the lang-name to see the language notes. Do you agree? not? make a pull request
 
|lang                    |RE-I |RE-NO|RE-LA|Meta-power|RT-speed|Syntax-flex.| 
|---------------------   |----:|----:|----:|---------:|-------:|--------:|
|[C-lang](lang/C.md)     |  50 |  40 |  20 |       35 |    100 |  70 |
|[LISP](lang/lisp.md)    |  30 |  20 |   5 |      100 |     30 | 100 |
|[C++](lang/CPP.md)      |  50 |  40 |  20 |       50 |     95 |  70 |
|[Python](lang/python.md)|  95 |  90 |  90 |       40 |      2 |  ?? |
|[Javascript](lang/js.md)|  60 |  35 |  10 |       40 |     25 |  80 |
|[Go-lang](lang/go.md)   |  65 |  60 |  ?? |       20 |     50 |  ?? |

