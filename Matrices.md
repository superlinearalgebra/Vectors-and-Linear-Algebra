# Introduction of Matrices

Matrices are an array of numbers arranged in order to represent numbers. We use matrices in different fields of science to solve problem. In Mathematics, it is used to solve linear equations and solve different problems since matrices are a fundamental part of linear algebra. 

We have different types of matrices, but one we focus on is very important. This will help you open up to linear algebra fields such as higher-dimension geometry and applied mathematics. 

# Augmented Matrix

An augmented matrix is an array of numbers inside brackets that represent a system of linear equations. Supposed we have a system of linear equations. We have to solve these system of equations by doing simultaneous equations. The question is how is that related? It's because we use an augmented matrix. However, how do we do operations in an augmented matrix? Simple. We have a process or a theorem. 

$\begin{pmatrix}
    a_{11}x_{1} & a_{12}x_{2} & \cdots & a_{1n}x_{n} &\bigm| & b_{1} \\
    a_{21}x_{1} & a_{22}x_{2} & \cdots & a_{2n}x_{n} &\bigm| & b_{2} \\
    \vdots & \vdots & \ddots & \vdots &\bigm| & \vdots \\ 
    a_{n1}x_{1} & a_{n2}x_{2} & \cdots & a_{nm}x_{n} &\bigm| & b_{m}
\end{pmatrix}$

However, we only use this to understand the concept of row operations and a method called **row-reduced echelon form**. It's basically reducing each row until you get a 1. We can do this by the rules of matrix row operations. We never usually use columns but uses rows as our method of doing operation to turn a matrix to RREF. RREF is a shorter way of saying reduced-row echelon form. 

# Matrix Arithmetic

Before we get into row operations we need to learn the operation of matrices. Adding and subtracting matrices is simple so as the same as scalar multiplication. 

$\begin{pmatrix}
    a & b & c \\
    d & e & f \\
    g & h & i
  \end{pmatrix}
    +
    \begin{pmatrix}
        j & k & l \\
        m & n & o \\
        p & q & r
    \end{pmatrix}
    =
        \begin{pmatrix}
        a + j & b + k & c + l \\
        d + m & e + n & f + o \\
        g + p & q + h & i + r
        \end{pmatrix}$

Remember your vector axioms from another tourist guide? Matrices are associative and commutative under addition or subtraction, same for vectors. The difference is in multiplication. The multiplication of two vectors is known as the cross product. The multiplication of matrices are way different than you may think. For starters, you can only multiply matrices if they are the same size. However in this tourist guide we only focus on $ n \times n$ matrix, since we are diving deeper in linear algebra. 

There is one axiom in matrices is that matrices are not commutative when multiplied. Here is an example. 

Let $\mathbf{A}$ and $\mathbf{B}$ be matrices living in $\mathbb{R}^3$. Let's say we want to find $\mathbf{AB}$. Simple. This is how we do it:

$\mathbf{A} = \begin{pmatrix}
                a & b & c \\
                d & e & f \\
                g & h & i
                \end{pmatrix}$

$\mathbf{B} = \begin{pmatrix}
                j & k & l \\
                m & n & o \\
                p & q & r
                \end{pmatrix}$

We need to find the value for $\mathbf{AB}$. So, we have a rule in matrices that we multiply by forming a 7-shape pattern. 

$\mathbf{A}\mathbf{B} = \begin{pmatrix}
                            aj + bm + cp & ak + bn + cq & al + bo + cr \\
                            dj + em + fp & dk + en + fq & dl + eo + fr \\
                            gj + hm + ip & gk + hn + iq & gl + ho + ir \\
                            \end{pmatrix}$

When you multiply, follow this rule: Multiply the first row with the first column then repeat this for second and third columns. Repeat the process again for the second and third rows, following the steps like we did with row 1.


There is one thing that you must note in this guide to matrices. $\mathbf{AB} \neq \mathbf{BA}$ in most cases. Some cases may work but why does this happen. What makes matrix multiplication different than any multiplication? 

**Activity 1**: We need to prove that matrix multiplication is not commutative. How can we do this? From your logic (if you are conscious during this time) we can say:

$\mathrm{A} =$ Matrix multiplication is commutative

$\neg \mathrm{A} =$ Matrix multiplication is not commutative. 

In groups of 5, discuss with your peers on how can you prove by contradiction in matrix multiplication. (Hint: consider $\mathbf{AB} = \mathbf{BA}$). 

**Discussion for Activity 1**: After discussing this with your friends, gather your results and we will go through step by step. 

Firstly consider we have two 2 by 2 matrix. You can do a 3 by 3 matrix, but I use a 2 by 2 so that tourists would not freeze to death due to the aura of a 3 by 3 matrix. 

$\mathbf{A} = \begin{pmatrix}
                1 & 2 \\
                3 & 4
               \end{pmatrix}$

$\mathbf{B} = \begin{pmatrix}
                6 & 7 \\
                8 & 9 
                \end{pmatrix}$

$\mathbf{AB} = \begin{pmatrix}
                24 & 25 \\
                50 & 57 
                \end{pmatrix}$

$\mathbf{BA} = \begin{pmatrix}
                27 & 40 \\
                35 & 52
                \end{pmatrix}$

We can see that $\mathbf{AB} \neq \mathbf{BA}$ because the values of $\mathbf{AB}$ and $\mathbf{BA}$ are not the same. This suggests that matrix multiplication is not commutative. We can denote that: $\mathrm{A} \implies \neg \mathrm{A}$. 

We proved this in $\mathbb{R}^2$ but how about in $\mathbb{R}^3$? The answer is it will be the same. Even if you keep proving it, it's not going to work. This is because matrix multiplication is not commutative regardless how many dimensions you have. $\mathbb{R}^2, \mathbb{R}^3, \mathbb{R}^4, \dots, \mathbb{R}^n$ would have the same rule. 

We have covered some matrix operations. Now we will turn matrices to some technical work. Be sure to stay awake. It's a long discussion. 

# Row Echelon Form, Reduced Row Echelon Form, Pivot, and Types of Solutions

Since mathematicians are lazy which is a good thing, we can say Row Echelon Form as REF and Reduced Row Echelon Form as RREF. The difference between REF and RREF is the numbers. REF is where there is a 1 in the beginning of the 1st row and the others can be other numbers. There will be leading 1s in the right and the left must be zero. RREF can be achieved when the forward phase is already in REF. We can do back substitution, but from REF you can do more row operations to reduce it to RREF. This may be complicated to you but with practice this should be easy. Keep in mind that you need to use valid row operations. We can talk about this. 

In this phase you are able to add and subtract rows, multiply a row with a number (we call it scalar), and swap rows. You can do two row operations simultaneously but not three. There are tips in this. 

Tips for Row Operations:

1. Before starting to do row operations, read the question and notice the numbers. 
2. When you swap rows, ensure you swap rows as your only row operation. Don't do any addition and sutraction of rows. 
3. Ensure that you form a zero and leading 1s in the right by doing proper row operations. 
4. Think about eliminating numbers by multiplying rows by its common factor and subtract rows. 
5. When you done, you must have leading 1s in the right and the rest are variables. 

When to stop: 

You can stop doing row operations to achieve RREF when the matrix has an inconsistent result. You can stop once you have a free variable or if you have all zeroes in the third row. This means you will have solutions and we will discuss them now. 

When you reduce a matrix to RREF, you can notice there is something that is familiar. Let's say we reducing a matrix:

$\begin{pmatrix}
    2 & -3 & 1 & 6 \\
    1 & 2 & 4 & -4 \\
    1 & -5 & -3 & -10
    \end{pmatrix}$

How can we know that this system of linear equations have a unique solution, no solutions, or infinitely many solutions? You do RREF. I have done this for you:

$\begin{pmatrix}
    1 & 0 & 2 & 0 \\
    0 & 1 & 1 & -2 \\
    0 & 0 & 0 & 0
    \end{pmatrix}$

The answer is obvious. This matrix shows that the systems of linear equations have infinitely many solutions because the zeros on the third row are consistent with the rows. We can say that the solutions are $(x,y,z) = (2s,-2-s,s)$. We can take a common factor out and conclude that we have a solution of: $(x,y,z) = (0,-2,0) + s(-2,-1,1)$. If you can notice, this is a vector equation of a line!!! This means that the infinitely many solutions form a line as its solution. Linear algebra is surely amazing. 

However, not all systems of equations can form either a unique solution or infinitely many solutions. This is because either the line in $\mathbb{R}^2$ or a plane in $\mathbb{R}^3$ does not have a common intersection point (or a unique solution). Since we have a tool such as REF and RREF to reduce an augmented matrix to its RREF form, we can talk about types of solutions. However we have new definitions:

**Definition of a free variable**: A free variable is a variable where there is no corresponding leading entry in the RREF form of an augmented matrix. 

**Definition of a leading variable**: A leading variable has a corresponding entry in the RREF in the augmented matrix. 

With these definitions, we can identify which ones are the free variables and the leading variable. Consider the augmented matrix:

$\begin{pmatrix}
    1 & 0 & 2 & 0 \\
    0 & 1 & 1 & -2 \\
    0 & 0 & 0 & 0
    \end{pmatrix}$

We can see that the third row has the entires of:
$\begin{bmatrix}
    0 & 0 & 0 & 0
    \end{bmatrix}$
which we conclude that there are infinitely many solutions. This is because our third row has consistent results. An inconsistent result would mean that this system of linear equations have no solutions. 



