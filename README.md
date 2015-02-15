Meta-Programming
================

Most programming languages allows you to write code on two levels: 

* Run-Time code: "RT-code" aka "ground level": the actual code you're focusing on.

* Compile-Time code: "CT-code" aka "meta-programming", "level 1": macros, preprocessor, code generation, templates, generic programming.

This two levels have **completely different** *domains*. This is a fundamental distinction, and something you must be aware-of in order to avoid destroying your productivity.

Level Domain
------------

Ground Level
************
Run-time programming (RT-code) domain is whatever problem you are working on. On RT-level, you write code which will solve the problem you are working on. 

RT-code primary domain is normally the "intended original purpose" of the language you're using, e.g.: general purpose, operating systems, symbolic list processing, formula translation, business processes, database query, database procedures, GUI-glue, etc.

Level 1
********
**Compile-time programming (CT-code) domain is the RT-code itself**. You work with blocks of RT-code. You can operate on them, generate RT-code by code or generate RT-code by template. CT-code is meta-programming, you write code which will generate code which will solve the problem you're working on.  

Measures
--------
In this github repository I will collect a list of programming languages with:

a) Their "intended original purpose" ("IOP")
b) the power-level of their meta-programming tools ("CT-Power")
c) the RT-speed (measured against C-lang)
d) a Readability score
d) Syntax-flexibility score

All values are measured in a 0 to 100 scale. Where 0 is no-power and 100 is full-power.

RT-speed
********
RT-speed is measured in a scale from 0 to 100, where 100 is *C-lang* speed. Example: RT-speed=50 means the RT runs at half the speed of a similar algorithm coded in C-lang.

Speed is measured for multi-core 64-bit processors.

Readability
***********
Readability is tricky to measure. The idea is to evaluate how easy is to understand "what the f\*#& the code is doing" by just reading it. The "canonical subject" reading the code is a programmer with basic experience on the language. There are three measures of readability: 

   1) RE-I: Readability "intended". When you use the language as designed *without abusing* syntax constructions and meta-programming tools.

   2) RE-NO: Readability "naturally occurring". (aka the "other world"). Real-word examples of language usage. It measures how readable ends up the code *when you’re solving real-world problems* (instead of writing "hello world" examples). i.e.: The linux kernel is a good example of RE-NO for C-lang.
   
   3) RE-LA: "Resistance to language abusing". Measures how resistant the language is when a "clever" programmer decides to "use to the fullest" (abuse) syntax constructions and meta-programming tools. Low RE-LA means a "clever" programmer can abuse the language into unreadability, High RE-LA means the language fights back, or has less-flexibility. 

Normally there's a **trade-off** between **readability** and **CT-power + syntax-flexibility**.

Syntax-flexibility
******************
Syntax-flexibility score intends to measure how "flexible" are the language syntax constructs. 
For example, C-lang’s type definition syntax is composable and highly-flexible. You can write: `void (*signal(int, void (*fp)(int)))(int);` which means "signal is a function passing an int and a pointer to a function passing an int returning nothing, returning a pointer to a function passing an int returning nothing". (http://c-faq.com/decl/spiral.anderson.html)

The example above shows high-syntax-flexibility leading to low readability. (for the "canonical programmer") (http://blog.golang.org/gos-declaration-syntax)

Other indicators of high syntax flexibility is: "everything is a function", "closures", "homoiconicity" and "there is more than one way to do it" (http://ceronman.com/2012/09/17/coffeescript-less-typing-bad-readability)
 
The problem is that **high syntax flexibility normally implies low readability (RE-NO and RE-LA mostly)**.


Collaborate
-----------
The language list is ridiculously short and the scores are arbitrary.

Please edit this repo. Either to add languages or to add more info. 

Pull requests are welcomed. Try to remain objective and not to stretch definitions to benefit one language or another.

Language Table

| lang                 | CT-power | RT-speed | RE-I | RE-NO | RE-LA | Syntax-flex.| 
|----------------------|---------=|---------=|-----=|------=|------=|------------=|
| [C-Lang](C-lang.rst) |  10      | 100      |  70  |  50   |  30   |  70         |
| [LISP](lisp.rst)     | 100      |  30      |  20  |  10   |   5   | 100         |
| [C++](CPP-lang.rst)  |  50      |  95      |  70  |  40   |  20   |  70         |
| [Python](python.rst) |   5      |   2      | 100  |  90   |  90   |  50         |
| [Javascript](js.rst) |  40      |  25      |  60  |  50   |  10   |  80         |

