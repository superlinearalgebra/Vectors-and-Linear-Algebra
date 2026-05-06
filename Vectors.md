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

# Abstract Vector Spaces - Definitions and Axioms

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

$\|\mathbf{u} \| = \sqrt{\mathbf{u}^2_1,\mathbf{u}^2_2, \dots, \mathbf{u}^2_n} \in \mathbb{R}^n$

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

We can use the vector equation to do things such as a point and a line or the most Cambridge of them all which is the shortest point to a line. We will discuss this later on. To understand vectors in a line, we must know the geometrical interpretation of vectors.

# Geometrical Interpretation of Vectors

There are things that you need to know and must be remembered. This topic will also cover the geometrical interpretation of vectors. What is geometrical interpretation?

Geometrical interpretation is where we interpret a mapping of a image living in $\mathbb{R}^n$. Let's start with what happens to the dot product. 

Let $\mathbf{u}$ and $\mathbf{v}$ be vectors living in $\mathbb{R}^n$. If we return to the fact that the dot product of these vectors equals to zero, then we can say the two vectors are orthogonal.

**Definition: Orthogonality is when two vectors are perpendicular to each other.**

Since $\cos{0} = \frac{\pi}{2}$, this means that these two vectors are orthogonal to each other. If you see this then we need to see the behaviour of $\cos{\theta}$ as $\mathbf{u\cdot v} < 0$ and $\mathbf{u\cdot v} > 0$. 

# Lines (Point in a Line and Intersection between two lines)

After a brief tangent of exploring geometric intepretation of vectors, we can explore how we can evaluate the point that is in the line. We can also evaluate the coordinates of the two vector lines intersecting each other. We also can solve problems based on shortest distance from a point to a line. Let's do that as an example. 

Let $\overrightarrow{OP}$ and $\overrightarrow{ON}$ be position vectors. Let $\mathnormal{l}$ be the line of a vector equation. All these vectors are living in $\mathbb{R}^3$.

$\overrightarrow{OP} = \begin {pmatrix}
                        11 \\
                        -5 \\
                        -3
                         \end {pmatrix}$

$\mathnormal{l} = \begin {pmatrix}
                    1 \\
                    5 \\
                    0
                    \end {pmatrix}
                + \lambda \begin {pmatrix}
                            -3 \\
                            1 \\
                            4
                            \end {pmatrix}$

If we look at the equation, we can see that N lies in the point and P must be perpendicular to N. So we can say that:

$\overrightarrow{ON} = \begin {pmatrix}
                        1 - 3\lambda \\
                        5 + \lambda \\
                        4\lambda
                        \end {pmatrix}$

We should have no problem finding $\overrightarrow{PN}$ since we can use a rule we remember to find $\overrightarrow{PN}$. 

$\overrightarrow{PN} = \overrightarrow{ON} - \overrightarrow{OP}$

$\overrightarrow{PN} = \begin {pmatrix}
                        1 - 3\lambda \\
                        5 + \lambda \\
                        4\lambda
                        \end {pmatrix}
                        - \begin {pmatrix}
                            11 \\
                            -5 \\
                            -3 
                            \end {pmatrix}$

Which results to:

$\overrightarrow{PN} = \begin {pmatrix}
                        -10 - 3\lambda \\
                        10 + \lambda \\
                        3 + 3\lambda
                        \end {pmatrix}$

We need to use the dot product to find $\lambda$ and see what values of $\lambda$ that makes $\overrightarrow{PN}$ **orthogonal**. The only solution is to compute $\overrightarrow{PN} \cdot \mathnormal{l}$. The problem is that the line $\mathnormal{l}$ is a line and what values should we take for our dot product? Well it is simple. We only take the direction vector only instead of the original vector. So something multiplied by the coefficient $\lambda$. 

$\overrightarrow{PN} \cdot \mathnormal{l} = \begin {pmatrix}
                                            -10 - 3\lambda \\
                                            10 + \lambda \\
                                            3 + 4\lambda
                                            \end {pmatrix}
                                            \cdot
                                            \begin {pmatrix}
                                            -3 \\
                                            1 \\
                                            4
                                            \end {pmatrix}
                                            = 0$

Now we use the rule of dot products and we have $\lambda = -2$ and we substitute $\lambda$ to $\overrightarrow{PN}$

$\overrightarrow{PN} = \begin {pmatrix}
                        -4 \\
                        8 \\
                        -5
                        \end {pmatrix}$

Let's say we want to find the distance of $\overrightarrow{PN}$. We can just substitute the values in the column vectors and applied the distance formula in $\mathbb{R}^3$. 

Let $\overrightarrow{PN} = \begin {pmatrix}
                            \mathnormal{x} \\
                            \mathnormal{y} \\
                            \mathnormal{z} 
                            \end {pmatrix} \in \mathbb{R}^3$

$\|\overrightarrow{PN}\| = \sqrt{\mathnormal{x}^2 + \mathnormal{y}^2 + \mathnormal{z}^2}$

$\|\overrightarrow{PN}\| = \sqrt{(-4)^2 + (8)^2 + (-5)^2}$

$\|\overrightarrow{PN}\| = \sqrt{105}$

It is okay if it is in exact form. We will use exact form to be more friendly to tourists who are exploring vectors. 

The lines either intersect, parallel to each other or they are skew from each other. Skew lines means that the lines do not intersect. In the $\mathbb{R}^3$ world, if the values of the parameter $\mathnormal{t}$ which is the scalar of the directional vector show consistentency that means they intersect. They will not intersect even if the $\mathnormal{x}$ and $\mathnormal{y}$ values remain the same when the $\mathnormal{z}$ remains unchanged. This is a useful insight for vectors since we can apply this to solve some problems in linear algebra. 

Using vector equation of a line we can use this to find an equation of a plane. This is a crucial skill that you need to master so that you will understand why vectors are versatile. They are the fundamental aspects of linear algebra. 

# Planes

A plane is a sheet of a line living in $\mathbb{R}^3$. A good way to illustrate this is to take a two sheets of paper and make them parallel to each other. Next, form an inverted T sign and notice that in the sheet of paper it touches the other to form a line of intersections. What can you conclude in this illustration?

We can say that planes can form a line of points. This means that there are infinite solutions in the plane. Since it forms a solutions. Planes have the same geometric rule for vectors. Either they are parallel to each other. 

However, we wanted to find the vector that lives in the plane. There are three different ways. The first is to form parametric equation of vectors and do some elementary algebra (substitution or elimination techniques), the second way involves the point normal equation and this only works if the normal is orthogonal to every other point in the plane. The third way is by using the cross product, also known as the determinant method (I call this the painful method). 

Let's find a general equation of a plane. We need an equation of a plane living in $\mathbb{R}^3$. We can obtain a general equation of a plane as:

$\mathnormal{A}\mathnormal{x}+\mathnormal{B}\mathnormal{y}+\mathnormal{C}\mathnormal{z} = \mathnormal{D}$

Where $\mathnormal{A},\mathnormal{B},\mathnormal{C}$ and $\mathnormal{D}$ are constants to be found. 

We can obtain a plane equation but how? We can use a line but there is a trick here. Let's say we have two vectors $\mathbf{u}$ and $\mathbf{v}$ living in $\mathbb{R}^3$. We can use these vectors to form an equation. Note that to form a plabe, both direction vectors are not **parallel** to each other. 

Let:

 $\mathnormal{x}_0 = (4,-2,3)$ 

 $\mathnormal{x}_1 = (1,-3,2)$

 $\mathnormal{x}_2 = (4,2,-1)$

 We can find both $\mathbf{u}$ and $\mathbf{v}$ by applying the rules we learn earlier. We know that:

 $\mathbf{u} = \mathnormal{x}_1 - \mathnormal{x}_0$

 $\mathbf{v} = \mathnormal{x}_2 - \mathnormal{x}_0$

 Looking at this: We conclude that we deduce a vector equation for a plane, that is:

 $\mathbf{u} = (-3,-1,-1)$

 $\mathbf{v} = (0,4,4)$

 Then we can use this formula:

 $\mathnormal{(x,y,z)} = \overrightarrow{\mathnormal{Ox}_0} + \mathnormal{t}_1\mathbf{v}_1 + \mathnormal{t}_2\mathbf{v}_2$

 $\mathbf{v}_1$ and $\mathbf{v}_2$ are just our $\mathbf{u}$ and $\mathbf{v}$ respectively. 

 So the vector equation for a plane is:

 $\mathnormal{(x,y,z)} = (4,-2,3) + \mathnormal{t}_1(-3,-1,-1) + \mathnormal{t}_2(4,2,-1)$

 Note that $\mathnormal{t}_1,\mathnormal{t}_2 \in \mathbb{R}$. This is all only true when both of the scalars are included in the reals. Another note that this is a vector equation situated in $\mathbb{R}^3$. Equations in $\mathbb{R}^2$ are just a line and it is easier to find. This means that we must find a plane. There are two ways. Either you do the cross-product or we can solve in a rigorous way by substituting values. This means we have to convert our vector equation of the plane to a parametric equation. This is the first step to find the equation of the plane.

$\mathnormal{x} = 4 - 3\mathnormal{t}_1 + 4\mathnormal{t}_2$

$\mathnormal{y} = 4 - \mathnormal{t}_1 + 2\mathnormal{t}_2$

$\mathnormal{z} = 3 - \mathnormal{t}_1 - \mathnormal{t}_2$

Notice that we can equate the first and second equation. First we multiply by 2 for the 2nd equation and the third equation we can multiply by 2. Subtract Equation 1 and 2 then add equation 3. This is how the steps look like:

$\mathnormal{x}- 2\mathnormal{y} = -4 - \mathnormal{t}_1$

$\mathnormal{y} + 2\mathnormal{z} = 7 - 3\mathnormal{t}_1$

Then we can multiply the equation $\mathnormal{x} - 2\mathnormal{y} = -4 -\mathnormal{t}_1$ by 3 to eliminate $\mathnormal{t}_1$. 

$3\mathnormal{x}- 6\mathnormal{y} - \mathnormal{y} - 2\mathnormal{z} = -12 - 7$

So the general equation of the plane is: $3\mathnormal{x} - 7\mathnormal{y} - 2\mathnormal{z} = -19$.

This is by far slightly more tedious than the cross-product, though the cross-product is by far the most fun. 

We can form general equation of a plane either by using a vector equation of a plane or we can use a point-normal equation. 

A normal vector is a vector that is **orthogonal** in every point in the plane. The point normal equation of a plane is:

$\mathnormal{A}(\mathnormal{x} - \mathnormal{x}_0) + \mathnormal{B}(\mathnormal{y} - \mathnormal{y}_0) + \mathnormal{C}(\mathnormal{z} - \mathnormal{z}_0) = \mathnormal{D}$.

This is only applicable if you have a normal vector which is orthogonal to a vector equation of a plane or just the plane itself. 

However, how do we find a plane in the most "linear algebra" method you will ever see in your time exploring vectors and linear algebra? We can use the cross-product. 

# Planes - Cross Products

This requires you a knowledge in determinants which is covered in another tourist guide for linear algebra: Matrices. 

Before we dive to cross products, I wanted to say that the best way of learning linear algebra is to treat maths in general as a visit to an art gallery. Why an art gallery you may ask? It's because Maths is all the art of the outputs painted in the canvas and all you do is to look at it! I am not an art student because I am a maths students studying in my first year. You have to visualise this by yourself, but it is fun. 

So the cross product is denoted by:

$\|\mathbf{a} \times \mathbf{b}\| = \begin {vmatrix}
                                    \mathbf{i} & \mathbf{j} & \mathbf{k} \\
                                    \mathnormal{a}_1 & \mathnormal{a}_2 & \mathnormal{a}_3 \\
                                    \mathnormal{b}_1 & \mathnormal{b}_2 & \mathnormal{b}_3 
                                    \end {vmatrix}$

To get the cross product, you must either use the Rule of Sarrus or co-factor expansion. We will cover the Rule of Sarrus in the Matrices guide, but I will show you how to do the co-factor expansion. 

This is how we do it:

$\begin {vmatrix}
    \mathbf{i} & \mathbf{j} & \mathbf{k} \\
    \mathnormal{a}_1 & \mathnormal{a}_2 & \mathnormal{a}_3 \\
    \mathnormal{b}_1 & \mathnormal{b}_2 & \mathnormal{b}_3 
    \end {vmatrix} 
    = 
    \mathbf{i} \begin {vmatrix}
                \mathnormal{a}_2 & \mathnormal{a}_3 \\
                \mathnormal{b}_2 & \mathnormal{b}_3
                \end {vmatrix}
    -
    \mathbf{j} \begin {vmatrix}
                \mathnormal{a}_1 & \mathnormal{a}_3 \\
                \mathnormal{b}_1 & \mathnormal{b}_3
                \end {vmatrix}
    +
    \mathbf{k} \begin {vmatrix}
                \mathnormal{a}_1 & \mathnormal{a}_2 \\
                \mathnormal{b}_1 & \mathnormal{b}_2
                \end {vmatrix}$

Usually you may end up with a determinant, so you must evaluate them. 


$\begin {vmatrix}
    \mathbf{i} & \mathbf{j} & \mathbf{k} \\
    \mathnormal{a}_1 & \mathnormal{a}_2 & \mathnormal{a}_3 \\
    \mathnormal{b}_1 & \mathnormal{b}_2 & \mathnormal{b}_3 
    \end {vmatrix} 
    = ((\mathnormal{a}_2\mathnormal{b}_3)-(\mathnormal{b}_2\mathnormal{a}_3))\mathbf{i} + ((\mathnormal{a}_1\mathnormal{b}_3)-(\mathnormal{b}_1\mathnormal{a}_3))\mathbf{j} + ((\mathnormal{a}_1\mathnormal{b}_2)-(\mathnormal{a}_2\mathnormal{b}_1))\mathbf{k}$

When we have a cross product of vectors, we can use the point of origin to find the equation of the plane. We must use this equation:

$\mathnormal{A}(\mathnormal{x} - \mathnormal{x}_0) + \mathnormal{B}(\mathnormal{y} - \mathnormal{y}_0) + \mathnormal{C}(\mathnormal{z} - \mathnormal{z}_0) = \mathnormal{D}$.

We use this equation because the cross-product of the vectors results in a normal vector. 

Let's say we want to find a plane using the cross product. Let's do some linear algebra. Given that we have the points

$\mathbf{a} = (3,2,4)$

$\mathbf{b} = (1,0,2)$

$\mathbf{c} = (2,2,-4)$

We need to form a vector equation of a plane. We need to find values for $\overrightarrow{AB}$ and $\overrightarrow{BC}$. We do this by using the axioms and concepts we covered in this topic. 

$\overrightarrow{AB} = (-2,-2,-2)$

$\overrightarrow{AC} = (-1,0,-8)$

Now we can form an equation of a line which is from the origin to the equation of these two vectors. 

$(x,y,z) = (3,2,4) + \lambda(-2,-2,-2) + \rho(-1,0,-8)$

Now we do the cross products. I use the variables $\rho$ and $\lambda$ to make life easier and as a tag of vectors that are the component of the **cross-products**. 

$\overrightarrow{AB} \times \overrightarrow{AC} = \begin {vmatrix}
                                                    \mathbf{i} & \mathbf{j} & \mathbf{k} \\
                                                    -2 & -2 & -2 \\
                                                    -1 & 0 & -8 
                                                    \end {vmatrix}$

We have to do the determinant which is easy. 

$\overrightarrow{AB} \times \overrightarrow{AC} = \mathbf{i} \begin{vmatrix}
                                                            -2 & -2 \\
                                                            0 & -8
                                                         \end{vmatrix}
                                             -
                                                \mathbf{j} \begin{vmatrix}
                                                            -2 & -2 \\
                                                            -1 & - 8
                                                         \end{vmatrix}
                                             +  \mathbf{k} \begin{vmatrix}
                                                            -2 & -2 \\
                                                            -1 & 0
                                                         \end{vmatrix}$
                                                    
So we get $16\mathbf{i} + 18\mathbf{j} - 2\mathbf{k}$ Or we can just write it as $(16,18,-2)$. Since we are determining the equation of the plane which is in $\mathbb{R}^3$, the normal vector will sit in the plane. We need to deduce the general equation of the plane that passes through the position vector/point $\mathbf{a}$. So, we use an equation we have seen before. 

$\mathnormal{A}(\mathnormal{x} - \mathnormal{x}_0) + \mathnormal{B}(\mathnormal{y} - \mathnormal{y}_0) + \mathnormal{C}(\mathnormal{z} - \mathnormal{z}_0) = \mathnormal{D}$.

We use the point-normal equation because we produced a normal vector. Now a bit of a tangent on why we have a normal vector is that if you see two vectors with an angle $\theta$, the cross product of these two vectors **will** form an orthogonal vector which is the normal vector. The vector must be orthogonal to the plane, so we can input then in the constants A, B, and C. Then we can use whatever information we have to find the general equation of the plane. 

$16(\mathnormal{x} - 3) + 18(\mathnormal{y} - 2) - 2(\mathnormal{z} - 4) = 0$

Since we don't know it yet, we let the RHS zero. Then we get the result of:

$16\mathnormal{x} + 18\mathnormal{y} - 2\mathnormal{z} = 76$

It is a simple task to do. This is the end of the basics of vectors in $\mathbb{R}^2$, $\mathbb{R}^3$, and $\mathbb{R}^n$. Now we are moving to advanced vectors and some mix of vectors and linear algebra. 

# Eigenvectors and Eigenvalues - An Introduction to Advanced Vectors and Linear Algebra

For tourists who are keen to explore deeper fields of linear algebra, if this suits you be prepared as it will be exceptionally difficult as concepts here get harder and harder. 

This topic requires some visualisation in your head. Imagine you have a wooden branch you found somewhere in the fields. You then saw another branch and decided to compare those in two. Notice that if you lay two sticks in the ground and you compare the sizes, let's say the second stick is longer than the first stick, you can deduce that something that is multiplied by the first stick is equal to something that is multiplied to the second stick. This relationship is called the eigenvalue and eigenvectors. Eigenvectors and eigenvalues are used in many branches of Mathematics and sometimes in other branches of Science and Engineering. 

First lets consider the statement that:

$\mathbf{A}\mathbf{x} = \lambda\mathbf{x}$

What can we do is that we multiply both sides by the identity matrix. 

$\mathbf{I}\mathbf{A}\mathbf{x} = \lambda\mathbf{I}\mathbf{x}$

