### Matlab Cheetsheet 
## Essential Mathematic functios
1. ``sym(fraction)`` - can be used to display the number in fraction. 

2. ``double(fraction)`` - will convert the fraction into decimal number. 

3. ``sqrt(n)`` - will find the square root of the number. 

4. ``nthroot(n,root)`` - Will find the nth root of a number. 

5. ``exp(n)`` - To find the exponent of a number. 

6. ``pretty(n)`` - To format the symbol properly

7. ``real(complexN)`` - you will get real part from the complex number

8. ``imag(complexN)`` - you will get real part from the complex number

9. ``abs(n)`` - To get the absolute value of the number

## Solve Algebraic Equation 

To solve the Algebraic equation ax^n .... + bx + c  

```
equation = [a b c]
root(equation)
```
## Solve system of linear Equations

ax+by = c 
dx+ey = f

|a   b|      | e |
|     | X =  |   | 
|c   d|      | f |

To solve the system of linear equations we can find X(x,y) 

```
Sol = inv(a)*b
sol = (a^-1)*b 
```

This can used for other orders aswell


## Solve system of linear Equations symb

ax^2+bx+c = 0 

a. To solve the equation 

```
syms x
sol = solve(a*x^2+b*x+c,x)
```
b. To solve multiple eqn

```
syms x 
syms y
[x y] = solve(x+y-2,x-y+4)
```
c.  

```
syms x
syms y
solution = solve(x+c*y-2,c*x-y+4)
```

