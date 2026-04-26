# Vectors and Linear Algebra
An essence to linear algebra.
We have the vector space with the euclidean vector space for 2-dimension and 3-dimension.
All of the topics for vectors require some understanding from Pure Mathematics 3 from Cambridge CIE A-Level. 

$A = 
    \begin{pmatrix}
    1 \\
    2 \\
    1
    \end{pmatrix}$

Vector A is a 3D vector. But is there anything we can improve to express our academic maturity? Well, we know what to do. 

$A = 
    \begin{pmatrix}
    1 \\
    2 \\
    1
    \end{pmatrix}$
in $\mathbb{R}^3$

This is how we say that the vector A is in $\mathbb{R}^3$ and in my notes we will focus more in $\mathbb{R}^2$, $\mathbb{R}^3$, $\mathbb{R}^4$ and $\mathbb{R}^n$ space. 

# Axioms of Vectors
in $\mathbb{R}^n$, vectors follow axioms in terms of addition, subtraction, and its properties when interating with other vectors. 

Vectors have an important property that it has a linear combination. We call these scalars. This is important for a unit vector, which we will cover after the axioms. 

Commutativity: $\mathrm{u} + \mathrm{v} = \mathrm{v} + \mathrm{u}$

Closure under addition: $\mathrm{u + v} \in \mathbb{R}^n$

Associativity: $\mathrm{(u + v) + w} = \mathrm{(u + v) + w}$

Existence of additive identity: $\mathrm{u + 0 = u}$

Existence of additive inverses: $\mathrm{u + (-u) = 0}$

Closure under scalar multiplication: $\mathnormal{a} \mathrm{u} \in \mathbb{R}^n$

Compatibility with field multiplication: $\mathnormal{a} \mathnormal{(b} \mathrm{u)} = \mathnormal{ab} \mathrm{(u)}$

Distributivity over vector addition: $\mathnormal{a} \mathrm{(u + v)} = \mathnormal{a} \mathrm{u} + \mathnormal{a} \mathrm{v}$

Distribitivity over scalar addition: $\mathnormal{(a + b)} \mathrm{u} = \mathnormal{a} \mathrm{u} + \mathnormal{b} \mathrm{u}$

We can see here that these properties are important so have a look and play by these rules. 

# Linear Combination of Vectors
This is not a complicated process as we can multiply a vector by a scalar. Let say we wanted to do this:

$A = 3\Bigg(\begin{pmatrix}
        2 \\
        3 \\
        -1
    \end{pmatrix}
    +
        \begin{pmatrix}
        2 \\
        1 \\
        -4
        \end{pmatrix}\Bigg)$

If we expand the brackets and apply scalar multiplication we can see the process of linear combination of vectors. 

$A = 3\begin{pmatrix}
        2 \\
        3 \\
        -1 \\
    \end{pmatrix} 
    +
    3\begin{pmatrix}
        2 \\
        1 \\
        -4
        \end{pmatrix}$

Doing the operations given by the axioms of vector addition:

$A = \begin{pmatrix}
        12 \\
        12 \\
        -13
        \end{pmatrix} \in \mathbb{R}^3$

This is how we use the axioms to evaluate the linear combination of column vectors. It is not necessary to say the column vector is part of the $\mathbb{R}^3$ space. Speaking of column vectors, there are many ways to express vectors rather than using column vectors. 

$\mathbf{u} = (\mathbf{u}_1, \mathbf{u}_2, \dots, \mathbf{u}_n) \in \mathbb{R}^n$

$\mathbf{u} = \mathrm{a}\mathbf{i} + \mathrm{b}\mathbf{j} + \mathrm{c}\mathbf{k}$ 

$\forall(\mathrm{a}, \mathrm{b}, \mathrm{c}) > 0 \in \mathbb{R}^3$

These are how you write vectors in the i, j and k notation and the other which is common in university courses. Different notation still result in the same answer. How does this relate to the linear combination of vectors? If we multiply a vector with a scalar the i,j,k and the first notation both are distributive. This means when you multiply over the bracket, you distribute the scalars to the vector value since the scalar increases the size to where the vector is directing. The i, j and k notation and column notation are common in the Cambridge CIE A-Level Maths and Further Maths course.

Linear Combination of Vectors or Scalar Multiplication increases the length of the vector but it also shows that the vectors are parallel. 

# Position Vectors and Theory
We covered through basic axioms and we will apply these to vectors as part of our progress through the world of linear algebra. 

A position a vector is a vector that is directed to the point from the origin. A zero vector is also known as the origin. With the formula $\mathbf{O} = (\mathbf{0},\mathbf{0},\dots, \mathbf{0}_n) \in \mathbb{R}^n$. 

How do we find the direction of two points given that we have two position vectors? We can use geometric intepretation but it may take a long time and in a time-pressured environment it would be nasty to do this. Since two position vectors can be operated by subtraction we can get the formula:

$\overrightarrow{OA} = (2,1,6)$ 

$\overrightarrow{OB} = (-1,4,3)$

$\overrightarrow{AB} = \overrightarrow{OB} - \overrightarrow{OA}$

$\overrightarrow{AB} = (3,-3,3)$

The second letter must be subracted by the first letter. Remember this rule. This applies to ANY vector. This is handy and it allow us to evaluate vectors easier. More on these when you work on your exercises. 

# Length of a Vector

The length of a vector is the distance between the origin to the point. We can evaluate the length of a vector with this formula

$\|\mathbf{u} \| = \sqrt{\mathbf{u}^2_1,\mathbf{u}^2_2, \dots, \mathbf{u}^2_n} \in \mathbb{R}^3$

Order does not matter since we are squaring it and square rooting the values. This is important for a component that we need to use to calculate the angle between two vectors. 

# Dot Product and Angle of a Vector

The dot product is the product of multiplying two vectors together. This creates a value that is important to find the angle or whether our vectors are obtuse, acute, or orthogonal. We will talk about orthogonality later on. Our rule of the dot product is that we will mulytoply both vectors together.  

$\mathbf{u\cdot v} = \begin {pmatrix}
                        \mathbf{u}_1 \\
                        \mathbf{u}_2 \\
                        \dots        \\
                        \mathbf{u}_n
                        \end {pmatrix}
            \cdot
                    \begin {pmatrix}
                        \mathbf{v}_1 \\
                        \mathbf{v}_2 \\
                        \dots        \\
                        \mathbf{v}_n
                        \end {pmatrix}
                    = (\mathbf{u}_1\mathbf{v}_1 + \mathbf{u}_2\mathbf{v}_2 + \dots + \mathbf{u}_n\mathbf{v}_n) \in \mathbb{R}^n$

We have the dot product of vectors. There is one speculation that you can do the dot product three times which is not possible. Who even thinks that three dot products exists. The reason behind this is that you have done the dot product twice so doing it three times doesn't make sense. If a dot product exists, doing the dot product again would end up with a scalar. 

We are finished with the dot product and now we move to the angle of a vector. How can we find the angle of a vector? Well, we have a formula which which is:

$\cos{\theta} = \frac{\mathbf{u\cdot v}}{\|\mathbf{u}\|\|\mathbf{v}\|}$

These will help us finding the angle about vectors. 

# Equation of a Line
We see that vectors point the direction to the point from the origin. We can manipulate this by making an equation of a line. This helps only if we have two things. First is the direction from origin to a point. This point can be anywhere so a position vector is necessary. The second thing is a line passing two points. For example: You can have a poing A with a line passing through B. This means that the line AB is part of the vector equation of a line. In the second sentence I wrote 'manipulate' and you may be confused why we 'manipulate' a vector equation. How do we manipulate?

We need to discuss two things. The first thing is that we want to know the general equation of a line in $\mathbb{R}^2$ and $\mathbb{R}^3$. The last thing is that how we can manipulate this equation with or without drawing a graph. This is especially troublesome for lines in $\mathbb{R}^3$. 

First is the general equation of a line in $\mathbb{R}^2$

$\mathrm{A}\mathnormal{x} + \mathrm{B}\mathnormal{y} = \mathrm{C}$ $\exists \mathrm{A,B} > 0 \in \mathbb{R}^2$

The last thing is the general equation of a line in $\mathbb{R}^3$. Be careful that it is either in the x,y or y,z axis. If you combine both then it will be a plane. 

$\mathrm{A}\mathnormal{x} + \mathrm{B}\mathnormal{z} = \mathrm{C}$

$\exists \mathrm{A,B} > 0 \in \mathbb{R}^3$

$\mathrm{A}\mathnormal{y} + \mathrm{B}\mathnormal{z} = \mathrm{C}$

$\exist \mathrm{A,B} > 0 \in \mathbb{R}^3$

But do we need more? Yes. We need something called a vector equation of a line. We do not need to worry as we can define:

$\overrightarrow{\mathbf{a}} = \overrightarrow{\mathbf{a}} + \mathrm{t}\overrightarrow{\mathbf{b}}$

This is good as we can use this as parametric equations. Parametric equations are equation on vectors in terms of any varible. If we look at the vector equation, we can get the x, y, abd z values in terms of t. Which means we are adding the two vectors to get the components of x, y, and z to form a parametric equation. It is easier to convert back to a vector equation. 

We can use the vector equation to do things such as a point and a line or the most Cambridge of them all which is thebshortest point to a line. We will discuss this later on. To understand vectors in a line, we must know the geometrical interpretation of vectors.

# Geometrical Interpretation of Vectors

There are things that you need to know and must be remembered. This topic will also cover the geometrical interpretation of vectors. What is geometrical interpretation?

Geometrical interpretation is where we interpret a mapping of a image living in $\mathbb{R}^n$. Let's start with what happens to the dot product. 

Let $\mathbf{u}$ and $\mathbuff{v}$ be vectors living in $\mathbb{R}^n$