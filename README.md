# Developing the Development Guide for Developers

## Standard
- License
    - Public projects: MIT
    - Private projects: Proprietary
    - Header on all source code files

- Soft tabs with 4 spaces

- SOLID

- Char encoding: UTF-8 without BOM

- Namespaces/Packages: Mandatory

- Naming conventions:

    - Class:      CamelCase
    - Variables:  camelBack
    - Functions:  camelBack
    - Constants:  UPPER_CASE


- Line break: Unix LF

- No spaces before LF

- Estruturas de controle
````javascript
if (!op1) {
    // code
    // code
}
if ((!op1) && (op2 || op3)) {
    // code
    // code
} else {
    // code
    // code    
}
````
````javascript
switch (expression) {
    case expression:
        // code
        break;
    default:
        // code
}
````
````javascript
for (i = 0; i < max; i++) {
    // code
}
````
````javascript
do {
    // code
} while (expression);
````
````javascript
while (op1 && !(op2 && op3)) {
    //  code
}
````
````javascript
// One liners
if (true)
    i = 1;    
````
````javascript
// Ternary
// Do not call actions on ternary returns
    y = x.isValid() ? x.getValue() : -1;
````

- Comments
````javascript
/**
 * Description of the function
 * One space before and after the asterisk
 *
 * @param Number x
 *
 * @return int
 */
 function square(x) {
     return x * x;
 }
````

## Boilerplate
- Front-end
    - HTML projects
    - JS module projects
- Back-end
    - Composer project
    - PIP project
    - Maven project
- Mixed (Front-end & Back-end)
    - Composer + NPM

## Language
    - PHP
    - Javascript
    - Java
    - Python

## Suggestions
    - Line length (120 characters)
    - Function length (40 lines)
    - Fonts: Hack, Fira Mono, Consolas, Inconsolata, Source Code Pro

## Optimizations
-   Avoid micro-optimizations
-   PREFER legibility over clever code
````python
    a = [1,2,3]
    ret = [fun(x) for x in someList]
    ret = []
    for x in someList:
        ret.append(fun(x))

    for value in variable:
        pass
    ret = [lambda x : x*x for x in someList]
````

## Actions

- Procurar por Linters (JSLint, PyLint, PHPCS, JAVA?)

- PR Ranking

- How to (Atom, Sublime, Eclipse, VIM, NetBeans)

- Cada um pega as particularidades da sua área

- Montar Boilerplates (Cássio, Flávio, Rafa)
    - Cauê::assistir(flavio);

- Flávio
    - Code review
