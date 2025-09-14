# Java Script Theory

1. Hoisting : in JavaScript refers to the behavior where variable and function declarations are moved (or "hoisted") to the top of their scope (global or function scope) during the compilation phase, before the code is executed.

    - Function declarations → Hoisted completely
    - var → Hoisted, initialized with undefined
    - let / const → Hoisted, but inaccessible until declared (TDZ)
    - Function expressions / Arrow functions → Hoisted like variables, not as functions

2. The Scope Chain, Scope & Lexical Environment

    - Scope of a variable is directly dependent on the lexical environment.
    - Whenever an execution context is created, a lexical environment is created. Lexical environment is the local memory along with the lexical environment of its parent. Lexical as a term means in hierarchy or in sequence
    - Having the reference of parent's lexical environment means, the child or the local function can access all the variables and functions defined in the memory space of its lexical parent
    - The JS engine first searches for a variable in the current local memory space, if its not found here it searches for the variable in the lexical environment of its parent, and if its still not found, then it searches that variable in the subsequent lexical environments, and the sequence goes on until the variable is found in some lexical environment or the lexical environment becomes NULL
    - The mechanism of searching variables in the subsequent lexical environments is known as Scope Chain. If a variable is not found anywhere, then we say that the variable is not present in the scope chain

3. `let & const in JS (Temporal Dead Zone)`

    - let and const are hoisted but its memory is allocated at other place than window which cannot be accessed before initialisation
    - Temporal Dead Zone exists until variable is declared and assigned a value
    - window.variable OR this.variable will not give value of variable defined using let or const
    - We cannot redeclare the same variable with let/const(even with using var the second time)
    - const variable declaration and initialisation must be done on the same line

    - There are three types of error:

        - referenceError {given where variable does not have memory allocation}
            - Like when accessing 'let' variables before declaration, as they were in TDZ (Temporal Dead Zone)
            - Like when accessing, a variable which is not declared (or present in code)
        - typeError {given when we change type that is not supposed to be changed}
            - Like re-assigning value to a const variable
        - syntaxError {when proper syntax(way of writing a statement) is not used}
            - Like when const variable is declared without initialisation

    - Use const wherever possible followed by let, Use var as little as possible(only if you have to). It helps avoid error
    - Initialising variables at the top is good idea, helps shrinks TDZ to zero
    - Level of strictness ... var << let << const

4. BLOCK SCOPE & Shadowing in JS
