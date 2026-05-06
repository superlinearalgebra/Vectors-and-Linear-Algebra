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

Another rule is that if you multiply matrices, the columns of the first matrix must be equal to the row of your second matrix. Then the rows of the first matrix and the columns of your second matrix is the resultant matrix. Order matters as we explained before. 

Matrices can only be added if they are in the same dimension. You cannot add a 3 by 3 matrix with a 2 by 2 matrix. 

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

You may be confused as if there are infinitely many solutions and you'd be right. However, in a higher dimension (e.g in $\mathbb{R}^3$), planes can either intersect at one point or intersect to form a line of solutions. We will talk about this later on in the future. How about no solutions, well the answer is that either the planes are parallel and not interesting or it does not have a common intersection even if one plane intersect at the other. 

Now we need to talk about pivots and its importance when doing REF and RREF. For an entry that is defined as a pivot, it must have two conditions. The first is that it must be a non-zero entry **moving from left to right**. The second is something that you may not heard of and will be difficult to understand which is column dominance. This is a mathematician's word for a condition in Gauss-Jordan elimination (or Gaussian Elimination). All entries below the pivot **must be zero**. 

# Matrix inverses

**WARNING:** This may involve some headaches and it takes some time. This is the most tedious sections of linear algebra. 

You can add, subtract, scalar multiplication, and matrix multiplication. However, how about dividing matrices? In matrices we rarely call it division but we call it inverse multiplication. In your elementary algebra, have you seen this?

$\mathnormal{a}^-1\cdot\mathnormal{a} = \frac{\mathnormal{1}}{\mathnormal{a}}\cdot\mathnormal{a} = 1$

This is the analogy. Rather than dividing by something how about multiplying by something inverse. Dividing is like multiplying by something raised to the power of -1. The problem is how can we find an inverse of a matrix? This may be a problem. But we need to backtrack to where we started which is about RREF. If we keep doing RREF to a matrix, we can get something like this:

$\begin{pmatrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1
    \end{pmatrix}$

This is called an identity matrix and this is helpful for finding an inverse. Notice that the inverse does nothing to a matrix which means it keeps the same value after multiplied. 

An inverse matrix can be like this:

$\mathnormal{I}_2 = \begin{bmatrix}
                        1 & 0 \\
                        0 & 1
                        \end{bmatrix}$

$\mathnormal{I}_3 = \begin{bmatrix}
                        1 & 0 & 0 \\
                        0 & 1 & 0 \\
                        0 & 0 & 1
                        \end{bmatrix}$

$\mathnormal{I}_4 = \begin{bmatrix}
                        1 & 0 & 0 & 0 \\
                        0 & 1 & 0 & 0 \\
                        0 & 0 & 1 & 0 \\
                        0 & 0 & 0 & 1
                        \end{bmatrix}$

$\mathnormal{I}_n = \begin{bmatrix}
                        1 & 0 & \cdots & 0 \\
                        0 & 1 & \cdots & 0 \\
                        \vdots & \vdots & \ddots & \vdots \\
                        0 & 0 & \cdots & 1
                        \end{bmatrix}$

For $\mathnormal{I}_n$, this is a general formula for an identity matrix living in $\mathbb{R}^n$-space. Consider the matrix $\mathnormal{A}$ and the vector $\mathbf{b}$ living in $\mathbb{R}^3$-space. If we make a system of linear equation we can write it as:

$\mathnormal{A}\mathbf{x} = \mathbf{b}$

This is a systen of linear equations defined if $\mathnormal{f}:\mathbb{R}^3 \to \mathbb{R}^3$. Other cases can be ignored. How can we make $\mathbf{x}$ by its own? This is a question you must ask yourself when attempting a question like this. We have no choice but to take an inverse of A. Which is denoted by $\mathnormal{A}^-1$. So the equation will look like this:

$\mathnormal{A}^{-1}\mathnormal{A}\mathbf{x} = \mathnormal{A}^{-1}\mathbf{b}$

$\mathnormal{I}_3\mathbf{x} = \mathnormal{A}^{-1}\mathbf{b}$

Since we know that the identity does nothing we can just conclude that:

$\mathbf{x} = \mathnormal{A}^{-1}\mathbf{b}$. 

From the methods of Gauss-Jordan elimination and RREF procedures you can know that we can find an inverse by making our original matrix an identity matrix while the identity as our inverse. Which requires row operations. 

Consider:

$\mathnormal{A} = \begin{pmatrix}
                    3 & -1 & 1 \\
                    1 & 1 & 1 \\
                    2 & 2 & 1 
                    \end{pmatrix}$

We know that $\{\mathnormal{A}\mid\mathnormal{I}_3\}$, which means we can start doing row operations.

$\begin{pmatrix}
    3 & -1 & 1 & \mid & 1 & 0 & 0 \\
    1 & 1 & 1 & \mid & 0 & 1 & 0 \\
    0 & 2 & 1 & \mid & 0 & 0 & 1
    \end{pmatrix}$

Now we need to find the inverse by doing row operations to reduce the LHS to $\mathnormal{I}_3$ and the RHS to be our $\mathnormal{A}^{-1}$. To do this we need to do row operations. 

$\mathnormal{R}_1 \leftrightarrow \mathnormal{R}_2$

$\mathnormal{R}_2 \to \mathnormal{R}_2 - 3\mathnormal{R}_1$

$\mathnormal{R}_3 \to \mathnormal{R}_3 - 2\mathnormal{R}_1$

$\mathnormal{R}_3 \to -\mathnormal{R}_3$

$\mathnormal{R}_2 \to \mathnormal{R}_2 + 2\mathnormal{R}_3$ 

$\mathnormal{R}_1 \to \mathnormal{R}_1 - \mathnormal{R}_3$

$\mathnormal{R}_2 \to -\frac{1}{4}\mathnormal{R}_2$

$\mathnormal{R}_1 \to \mathnormal{R}_1 - \mathnormal{R}_2$

The reason why I am showing you this is to show you how tedious it is. People said it is really long to do this and it requires an average of eight or nine steps to turn $\{\mathnormal{A}\mid\mathnormal{I}_3\}$ to $\{\mathnormal{I}_3\mid\mathnormal{A}^{-1}\}$ but there is a faster way. Before finding the laziest way of finding a matrix, we have to cover a couple of things about matrices. The question for you to reflect from here is can matrix **have no inverses?** Such question transcend human perspective from $\mathbb{R}^3$ to $\mathbb{R}^6$. 

## Matrix Invertibility

I hope you reflect on that question and write a couple of answers and also have a laugh at a joke I have. We mathematicians have a good sense of humour. Let's start on matrix invertibility. 

Let A be a matrix living in $\mathbb{R}^n$-space. A matrix is said to be invertible if $\mathrm{det}(\mathnormal{A}) \neq 0$. This is because if we look at a case of $\mathbb{R}^2$ which is:

$\mathnormal{A} = \begin{pmatrix}
                    a & b \\
                    c & d
                    \end{pmatrix}$

Finding the inverse is easy. The formula is:

$\mathnormal{A}^{-1} = \frac{1}{ad-bc}\begin{pmatrix}
                                        d & - b \\
                                        -c & a 
                                        \end{pmatrix}$
                            
Notice that when the case of a 2 by 2 matrix, we divide the diagonalised matrix by the determinant of it. This determinant determines if $\mathnormal{A}$ has an inverse. This is why we called this matrix an invertible matrix. Thus we define an invertible matrix as **a matrix that has a multiplicative inverse**. In the case of $\mathbb{R}^3$ and $\mathbb{R}^n$, this would be the same. Let's start in the case of $\mathbb{R}^3$. 

$\mathnormal{A} = \begin{pmatrix}
                    a & b & c \\
                    d & e & f \\
                    g & h & i
                    \end{pmatrix}$

Another shortcut to find the inverse is this:

$\mathnormal{A}^{-1} = \frac{\mathrm{adj}(\mathnormal{A})}{\mathrm{det}(\mathnormal{A})}$

You can see that cases in $\mathbb{R}^2$ and $\mathbb{R}^3$, the $\mathrm{det}(\mathnormal{A})$ has to be non-zero. This means we can say that the range of values for $\mathrm{det}(\mathnormal{A})$ is that $\mathrm{det}(\mathnormal{A}):\mathbb{R}\setminus \{0\} \to \mathbb{R}$.

However if $\mathrm{det}(\mathnormal{A}) = 0$ This means either we have no solution to the matrix or we have **infinitely many solutions**. This is when a matrix does not have a multiplicative inverse and considered as not invertible. 

# Determinants 

A determinant is a special scalar value that can be calculated from a square matrix. Why does this matter is that if we think of determinants geometrically, a 2 by 2 matrix will show an area of a parallelogram while a 3 by 3 show the volume of a parallelpiped (slanted box). We don't need to interpret a 4 by 4 matrix determinant since we don't visualise it much. 

To calculate a determinant of a 2 by 2 matrix is a simple thing to do. 

$\mathnormal{A} = \begin{pmatrix}
                    a & b \\
                    c & d
                    \end{pmatrix}$

$\mathrm{det(\mathnormal{A})} = \begin{vmatrix}
                                    a & b \\
                                    c & d
                                    \end{vmatrix}
                                = \mathnormal{ad} - \mathnormal{bc}$

Notice that after getting ad we have to subtract bc. This minus sign came out of nowhere. You might think this is true but no, this never happened. That is just because you don't know what a minor co-factor is. 

I want to take a case on a 2 by 2 matrix but the problem is that a 2 by 2 matrix is not really a problem. The problem is where you have a matrix that is 3 by 3. The thing is that how can I know that the cofactor is plus or minus? To visualise:

$\mathrm{det(\mathnormal{M})} = \begin{vmatrix}
                                    + & - & + \\
                                    - & + & - \\
                                    + & - & + 
                                    \end{vmatrix}$

So to calculate a determinant of a 3 by 3 matrix: consider a matrix $\mathnormal{M}$ that is invertible $\iff$ the $\mathrm{det(\mathnormal{M})} \neq 0$. To calculate the determinant:

$\mathnormal{M} = \begin{pmatrix}
                    a & b & c \\
                    d & e & f \\
                    g & h & i
                    \end{pmatrix}$

$|\mathnormal{M}| = \begin{vmatrix}
                        a & b & c \\
                        d & e & f \\
                        g & h & i
                        \end{vmatrix}$

We need to eliminate the first row, then the first column. The uneliminated numbers will be the 2 by 2 determinant **times** by the number that intersects the row and column eliminations. Repeat this until you reach the final number on the first row. Be mindful about the sign notation when you do this. This part is where most students make their mistakes on. If you cannot remember the sign comvention, create a 4 by 3 matrix with a plus minus checkerboard pattern. This should look like this:

$\mathrm{det(\mathnormal{M})} = \begin{vmatrix}
                                    + & - & + \\
                                    - & + & - \\
                                    + & - & + 
                                    \end{vmatrix}$
If this is helpful for you then good. If it is not, then use the Sarrus rule, which basically means you have to rewrite the first two columns and form a waffle pattern. I don't know how can I show you this but the co-factor expansion is better. Of course, it's invented by the French so it should be good (is it?). 

Since we have calculate a non-zero determinant, we have three things to cover:

1. The invertibility of a matrix (covered)

2. The image is the whole co-domain. 

3. Solving an original matrix. 

We covered the matrix invertibility part. Let's talk on how determinants can show you that it maps the image so that the image is the whole co-domain. 

A determinant is not just a volume scalar (for a 3 by 3 matrix) or area (for a 2 by 2 matrix). However, a determinant is also a "compression factor". If $\mathrm{det(\mathnormal{A})} \neq 0$ then this means that the transformation $\mathnormal{T(\mathnormal{M})}: \mathbb{R}^n \to \mathbb{R}^n$. This means that the transformation is **onto** (surjective). Other than that the transformation is not onto. From a 3D space turned to a 2D plane is not surjective. 

This is a bit harder to conceptualise, which is why I will combine with the vectors topic, since we will cover subspaces and vector spaces. Now we will cover one last thing for a determinant which is a solution to a matrix. 

If a matrix is not invertible, it will not have a multiplicative inverse and thus no solutions. This is why from a Cramer's rule, the determinant defines the invertibility of the 3 by 3 matrix. This is why when the determinant is zero, there is no inverse which means no solution. Remember this equation for matrix systems of linear equations:

$\mathnormal{A}\mathbf{x} = \mathbf{b}$

If we know that $\mathrm{det(\mathnormal{A})} \neq 0$, then we know that this system of linear equation gives a unique solution (one solution). You may think this is the end of the story and you conclude that the determinant is where the transformed matrix has a solution. Unfortunately, that is not the case. If $\mathrm{det(\mathnormal{A})} = 0$ then we know that there is no inverse so, no solution. However, if there is a non-trivial null space (kernel), then we have infinitely many solutions. If vector b is zero vector, then the case is that it has infinitely many solution because the null space is one-dimensional. You will learn this after covering co-factor and minors, in the study of euclidean spaces and rigorous linear algebra topics. 

So, we can conclude:

1. If $\mathnormal{A}$ has a non-zero determinant, then it will have a unique solution. 
2. Otherwise, it will have no solution due to inconsistency in the system due to the vector is not in the column space of $\mathnormal{A}$. 
3. In other cases, it will have **infinitely many solutions**. 

This is hard to grasp, covering hard concepts that are not easy and really unfriendly concepts to young math aspirants. This is the stage that you are trusted to handle the topics with maturity. Linear algebra is not for everyone. 

# Higher Linear Algebra I - Transformation and Linear Subspaces

In this to
