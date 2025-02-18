

# CMPS 2200 Assignment 1

**Name:** Mauricio Uribe


In this assignment, you will learn more about asymptotic notation, parallelism, functional languages, and algorithmic cost models. As in the recitation, some of your answer will go here and some will go in `main.py`. You are welcome to edit this `assignment-01.md` file directly, or print and fill in by hand. If you do the latter, please scan to a file `assignment-01.pdf` and push to your github repository. 
  
  

1. (2 pts ea) **Asymptotic notation** (12 pts)

  - 1a. Is $2^{n+1} \in O(2^n)$? Why or why not? 
.  Yes so we need to check 2^{n+1} is not in 0(2^n) The Big-O notation describes an upper bound on the growth rate of a function. To determine if 2^{n+1} is in 0(2^n), we need to check that there exist constants c and n0 such that: 2^{n+1} <= 2^n for all n>= n0 we can simplify and get 2<= c which means that c must be at least 2 therefore 2^{n+1} is in 0(2^n) with c = 2 and n0 =0, however, Big O notation typically ignores constant factors and lower ordered terms since 2^{n+1} = 2 x 2^n which is exactly twice 2^n, it grows at the same rate as 2^n but with a constant of 2, therefore, 2^{n+1} and 2^n are asymptotically equivalent and 2^n+1 is in 0(2^n)
.  
  - 1b. Is $2^{2^n} \in O(2^n)$? Why or why not?     
.  No 2^{2^n} is not in 0(2^n) because Big O notation describes an upper bound on the growth rate of a function so in order to determine if 2^{2^n} is in 0(2^n) we need to check if there exists a constants c and n0 such that 2^{2^n} <= c x 2^n then we simplify to 2^{(2^n) - n} <= c as n increases 2^n -n grows without bound causing 2^{(2^n)-n} to increase exponentially therefore no constant c can satisfy this inequality for all n therefore 2^{2^n} grows much faster than 2^n and is not in 0(2^n)
.  
  - 1c. Is $n^{1.01} \in O(\mathrm{log}^2 n)$?    
.  No, n^{1.01} is not in O((log n)^2) because big O notation describes an upper bound on the growth rate of a function. To determine if n^{1.01} is in O((log n)^2) we need to check if there exists a constant c and n0 such that n^{1.01} <= c x (log n)^2 for all n >= n0 as n increases n^1.01 grows polynomially while (log n)^2 grows logarithmically. Polynomial functions grow much faster than a logarithmic function as n becomes large. Therefore no constant c can satisfy this inequality for all n.
.  
  - 1d. Is $n^{1.01} \in \Omega(\mathrm{log}^2 n)$?  
.  Yes n^{1.01} is in Omega((log n)^2) because Big Omega notation describes a lower bound on the growth rate of a function. and to determine if n^{1.01} is in omega((log n)^2) we need to check if there exists a constant c and n0 such that n^{1.01} >= c x (log n)^2 for all n >= n0 as n increases, n^{1.01} grows polynomially while (log n)^2 grows logarithmicslly. Polynomial functions grow much faster than logarithmic functions as n becomes large. Therefore for a sufficiently large n, n^{1.01} will always be greater than or equal to c x (log n)^2 for some constant c
.   
  - 1e. Is $\sqrt{n} \in O((\mathrm{log} n)^3)$?  
.  No, sqrt(n) is not in O((\mathrm{log} n)^3) because in Big O notation describes an upper bound on the growth rate of a function. TO determine if sqrt(n) is in O((\mathrm{log} n)^3) we need to check if there exists a constan c and n0 such that sqrt(n) <= c x (log n)^3 for all n >= n0 as n increases, sqrt(n) grows polynomially while (log n)^3 grows logarithmically. Polynomical functions grow much faster than logarithmic functions as n becomes large. Therefore no contant c can satisfy this inequality for all n.
.  
  - 1f. Is $\sqrt{n} \in \Omega((\mathrm{log} n)^3)$?  
.  Yes, sqrt(n) is in Omega((\mathrm{log} n)^3), because Big Omega notation describes a lower bound on the growth rate of a function. SO to determine if sqrt(n) is in Omega((\mathrm{log} n)^3) we need to check if there exists contants c and n0 such that sqrt(n) >- c x (log n)^3 for all n >= 0. As n increases sqrt(n) grows polynomially while (log n)^3 grows logarithmically. Polynomial functions grow much faster than logarithmic functions as n becomes large. Therefore for a sufficiently large n sqrt(n) will always be greater than or equal to c x (log n )^3 for some constant c.

2. **SPARC to Python** (12 pts)

Consider the following SPARC code of the Fibonacci sequence, which is the series of numbers where each number is the sum of the two preceding numbers. For example, 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610 ... 
$$
\begin{array}{l}
\mathit{foo}~x =   \\
~~~~\texttt{if}{}~~x \le 1~~\texttt{then}{}\\
~~~~~~~~x\\   
~~~~\texttt{else}\\
~~~~~~~~\texttt{let}{}~~(ra, rb) = (\mathit{foo}~(x-1))~~,~~(\mathit{foo}~(x-2))~~\texttt{in}{}\\  
~~~~~~~~~~~~ra + rb\\  
~~~~~~~~\texttt{end}{}.\\
\end{array}
$$ 

  - 2a. (6 pts) Translate this to Python code -- fill in the `def foo` method in `main.py`  

  - 2b. (6 pts) What does this function do, in your own words?  

.  The function foo computes the fibonacci number for a given integer x. The fibonacci sequence is a series of numbers where each number is the sum of the two numbers beofre starting from 0 and 1.
.  
.  
.  
.  
.  
.  
.  
  

3. **Parallelism and recursion** (26 pts)

Consider the following function:  

```python
def longest_run(myarray, key)
   """
    Input:
      `myarray`: a list of ints
      `key`: an int
    Return:
      the longest continuous sequence of `key` in `myarray`
   """
```
E.g., `longest_run([2,12,12,8,12,12,12,0,12,1], 12) == 3`  
 
  - 3a. (7 pts) First, implement an iterative, sequential version of `longest_run` in `main.py`.  

  - 3b. (4 pts) What is the Work and Span of this implementation?  

.  
.  
.  
.  
.  
.  
.  
.  
.  


  - 3c. (7 pts) Next, implement a `longest_run_recursive`, a recursive, divide and conquer implementation. This is analogous to our implementation of `sum_list_recursive`. To do so, you will need to think about how to combine partial solutions from each recursive call. Make use of the provided class `Result`.   

  - 3d. (4 pts) What is the Work and Span of this sequential algorithm?  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  


  - 3e. (4 pts) Assume that we parallelize in a similar way we did with `sum_list_recursive`. That is, each recursive call spawns a new thread. What is the Work and Span of this algorithm?  

.  
.  
.  
.  
.  
.  
.  
.  

