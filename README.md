# Developing the Development Guide for Developers

## Standard
- License
    - Public projects: MIT
    - Private projects: Proprietary
    - Header on all source code files

- Soft tabs with 4 spaces

- SOLID
    + Single Responsibility Principle
    + Open Closed Principle
    + Liskov Substitution Principle
    + Interface Segregation
    + Dependency Inversion Principle

- Char encoding: UTF-8 without BOM

- Namespaces/Packages: Mandatory

- Naming conventions:

    - Class:      **CamelCase**
    - Variables:  **camelBack**
    - Functions:  **camelBack**
    - Constants:  **UPPER_CASE**

- **Line break: Unix LF**

- **No spaces before LF**

- Control Structures

````javascript
// When using one variable on an if statement
if (op1) {
    // code
    // code
}

// When using one variable and negating it on an if statement
if (!op1) {
    // code
    // code
}
````

````javascript
// Using more than one variable and expression in an if statement
if ((!op1) && (op2 || op3)) {
    // code
    // code
} else {
    // code
    // code    
}
````

````javascript
// One liner, do not use curly braces same applies to other control structures
if (true)
    i = 13;
else
    i = 31;
````

````javascript
// Swith statement
switch (expression) {
    case expression:
        // code
        break;
    default:
        // code
}
````

````javascript
// For statement
for (i = 0; i < max; i++) {
    // code
}
````

````javascript
// Do while statement
do {
    // code
} while (expression);
````

````javascript
// While statement 
while (op1 && !(op2 && op3)) {
    //  code
}
````

````javascript
// Ternary statement 

// Can do
    y = x.isValid() ? x.getValue() : -1;

// Can't do
// Do not call actions on ternary returns
    y = x.isValid() ? x.setValue() : -1;

````

- Comments
 
````javascript
 // This is the right way to do a comment
 //Don't comment like this

// JavaDoc standard 
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


## Suggestions (most of the suggestions are just personal, but it is good if you use it)
    - Line length (120 characters)
    - Function length (40 lines)
    - Fonts: Hack, Fira Mono, Consolas, Inconsolata, Source Code Pro

## VIM suggestions:
    - Use the following for your .vimrc (this uses 4 spaces instead of tabs):

    :set expandtab
    :set tabstop=4
    :set shiftwidth=4
    :set nu
    :set si

    " auto go back to last pos:
    if has("autocmd")
      au BufReadPost * if line("'\"") > 1 && line("'\"") <= line("$") | exe "normal! g'\"" | endif
    endif
    
    - To retab your document, transforming tabs into spaces issue the command :retab



## Python specific suggestions:

- Never, ever, ever do something like `from somewhere import *`. If you do that, there's no way to be sure what is getting imported and tools such as pylint become useless.
- You should install [pylint](https://www.pylint.org/) on your system.
- A file with metadata information about how checks are done can be generated with `pylint --generate-rcfile > ~/.pylintrc`
- That file can be edited to change the regular expressions for how variable names, function names, etc, are verified.
- I've had limited success with that...
- If using SublimeText, install the [SublimeLinter package](http://sublimelinter.readthedocs.org/en/latest/installation.html) and then the [SublimeLinter-pylint](https://github.com/SublimeLinter/SublimeLinter-pylint) plugin.
- Python naming conventions:
- Variable and function names should use camelCase convention
- Class names should use CapCase convetion
- Module and package names should use all lowercase, preferably without underscores.

## Java specific suggestions:
    - On Eclipse, go to Preferences > Java > Editor > Save actions and select:
    - Organize imports
    - Activate additional actions and click Configure:
    - Check remove trailing whitespace on all lines
    - Correct indentation
    - On the code style tab, mark:
    - Use blocks in if/while/for/do statements only if necessary
    - Use parentheses in expressions always
    - On the unnecessary code tab:
    - Remove unused imports should be checked.

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
## What not to do!

````c
    char a;float b,c;main(d){for(;d>2e3*c?c=1,scanf(" %c%f",&a,&c),d=55-a%32*9/5,b=d>9,d=d%13-a/32*12:1;a=2)++d<24?b*=89/84.:putchar(a=b*d);}
````

## Actions

* Search for Linters (JSLint, PyLint, PHPCS, JAVA?)

* PR Ranking

* How to (Atom, Sublime, Eclipse, VIM, NetBeans)

* Each member of the team will search for particularities of his area


* Build Boilerplates (Cássio, Flávio, Rafa)
````php
    $member = array(
        cassio,
        flavio, 
        rafa
    );
    caue::watch(member);
````
* Flávio
    * Code review