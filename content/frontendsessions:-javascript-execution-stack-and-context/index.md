---
title: "#FrontEndSessions: Javascript Execution Stack & Context"
description: "This ‘WTF is a …’ series is about learning by explaining. I’m adding teaching and explaining to my learning process so when I learn about a…"
date: "2020-02-09T14:00:57.128Z"
categories: []
published: false
---

This ‘WTF is a …’ series is about learning by explaining. I’m adding teaching and explaining to my learning process so when I learn about a concept or technology, I will attempt to explain it.

  

Will write about the Javascript execution context, execution stack, hoisting and scope. Makes sense that all these subjects area learnt together.

Wondered about how javascript really works, reduce the element of magic. help you understand what is going on when things don’t work. Improve yourself as a professional developer by knowing the core of how the tools you use work. 

Diagrams and code examples for each part. Use a context that has familiarity with a real non-nerd person

-   Intro and visualize about opening our console.log env, what the hell is happening? Whats the basic logic behind the process?

When we 1st run our code we create a **GLOBAL EXECUTION CONTEXT **

(Think of this as the world 🌍 our code lives in)

**(even if our program doesn’t have code)**

2 properties:  
\- window: global object  
\- this: window object

  

-   **thread of execution, (parsing and executing code line by line)**
-   **Live memory of variables and data. (Global variable environment)**

“Allows JS Engine to manage the complexity of interpreting and running our code”

When you run a function you create a **local execution context** for that function. This has local memory and a local thread of execution.

(Evaluated result is result of a function)  
After the code has been executed, the function’s local execution context gets erased and the output value gets stored in global memory

### Global Execution Context

(Each execution context has 2 Phases it goes through in an order)

-   Creation Phase
-   Execution Phase

**Creation Phase:**  
JS Engine will always create a global execution context

consists of   
window = global object  
this ==window (context object)

In this phase, 

-   create object called this
-   creates a global object
-   Memory space is set aside for variables and functions
-   Variables are assigned default values of undefined until execution phase & functions declarations are put entirely into memory

**Execution Phase:  
**2nd step

Javascript engine starts executing the code line by line.   
\- variables get assigned the values as they are parsed line by line  
\- parsed until no more variables and functions to parse.

The process of dealing with the initial variable declarations is called hoisting. — The process of assigning a variable declaration a default value of “undefined” during the Creation Phase.

### Local (function) Execution Context

Only time execution contexts are created are when the prorgram is first run (global) and whenever a local execution context is created

-   Create an arguments object
-   create object called this
-   Memory space is set aside for variables and functions
-   Variables are assigned default values of undefined until execution phase & function declarations are put entirely into memory

When a function is invoked, a new execution context is created. When its finished running through the lines of code in the function. The local execution context is wiped from memory.

When you pass a variable in from an outer “context”, it gets put into the memory of the local execution context, already assigned as its value and not undefined.

This is probably the best place to introduce scope.

### Scope

Talk abour trying to reference an inner variable from a function outside of it after it has already been invoked.  
The variable that exists has already been cleared from memory as that function that has been invoked has already been popped off the call stack.

Second Example, 

  
What if the variable its looking for is not in the current execution context?

If the variable is not found in the current execution context, it follows the **scope chain** to the execution context above that encloses over the current one and checks its context. This keeps on going until it finds the variable declared or it reaches the global execution context. If it doesn’t exist, it will throw a reference error.

What happens when you have a functionInner(Y) inside a functionOuter(x)?  
The Javascript Engine creates a Closure Scope. This is where the inner function creates a closure around the outer functions execution context. This allows it to have access to its local execution context in regards to the variables stored in memory. 

When it comes to the part of executing the return function of the HOC, it will look for any variables that are not in its execution context by following the Closure Scope. It can follow the scope chain and access the variables needed in the closest parent execution context.

  

What happens when there are many functions? How does JavaScript engines keep track?

Its time to introduce the Execution Stack (or Call Stack)

### Call Stack 

**(A list of executions to be ran)**

-   Whatever is top of the call stack, is what is getting executed.
-   Last thing that gets put in, last thing that gets taken out. (Push n pop)

  
\- **Hoisting**. (Important to understand)  
 — The process of assigning a variable declaration a default value of “undefined” during the Creation Phase.   
Javascript only hoists declarations.  
variables initialized with `var`get hoisted to the top of the global scope.   
Instances of `var` and `let` can be initialised without assigning value (and if you try to call it, it will return `undefined`) but instances of const can not be initialized without assigning a value(So if you try to access that reference, the engine will throw a reference error).

Variable Declarations get hoisted but their assignment expressions don’t.  
Hence why if you call a variable before it gets declared..we dont get a reference error, we get undefined.  
**Code Examples & Diagrams**

###
