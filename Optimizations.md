# Optimizations
- Avoid micro-optimizations
- PREFER legibility over clever code

## What to do
```python
    a = [1,2,3]
    ret = [fun(x) for x in someList]
    ret = []
    for x in someList:
        ret.append(fun(x))

    for value in variable:
        pass
    ret = [lambda x : x*x for x in someList]
```
## What NOT to do
```c
    char a;float b,c;main(d){for(;d>2e3*c?c=1,scanf(" %c%f",&a,&c),d=55-a%32*9/5,b=d>9,d=d%13-a/32*12:1;a=2)++d<24?b*=89/84.:putchar(a=b*d);}
```
