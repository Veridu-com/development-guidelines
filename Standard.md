# Development Standard

## License
- Public projects: MIT
- Private projects: Proprietary
- Header on all source code files

## Editor
- Soft tabs with 4 spaces
- Char encoding: UTF-8 without BOM
- Line break: Unix LF
- No spaces before a LF

## Concepts
- Namespaces/Packages: Mandatory
- SOLID
    + Single Responsibility Principle
    + Open Closed Principle
    + Liskov Substitution Principle
    + Interface Segregation
    + Dependency Inversion Principle

## Naming Conventions
- Class:      **CamelCase**
- Variables:  **camelBack**
- Functions:  **camelBack**
- Constants:  **UPPER_CASE**


## Control Structures

```javascript
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
```

```javascript
// Using more than one variable and expression in an if statement
if ((!op1) && (op2 || op3)) {
    // code
    // code
} else {
    // code
    // code
}
```

```javascript
// One liner, do not use curly braces same applies to other control structures
if (true)
    i = 13;
else
    i = 31;
```

```javascript
// Swith statement
switch (expression) {
    case expression:
        // code
        break;
    default:
        // code
}
```

```javascript
// For statement
for (i = 0; i < max; i++) {
    // code
}
```

```javascript
// Do while statement
do {
    // code
} while (expression);
```

```javascript
// While statement
while (op1 && !(op2 && op3)) {
    //  code
}
```

```javascript
// Ternary statement

// Can do
    y = x.isValid() ? x.getValue() : -1;

// Can't do
// Do not call actions on ternary returns
    y = x.isValid() ? x.setValue() : -1;

```

## Comments

```javascript
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

```
