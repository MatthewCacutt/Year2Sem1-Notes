# Deflection of Beams
The equation for the curvature of a beam is given by
$$
\frac{d^2y}{dx^2}=\frac{M(x)}{EI}
$$
where $M(x)$ is the equation for the bending moment throughout a beam,
$E$ is the young's modulus of the beam's material,
and $I$ is the area moment of inertia of the cross section of the beam.

This equation is only true for constant values of $E$ and $I$.

## Area Moment of Inertia
The Area Moment of Inertia is a property describing the distribution of a shape's area relative to an axis. The further material is away from the axis through which a beam is bending, the more resistance to bending it will have in that axis though it should be noted that at extremes, problems with buckling and bending may occur in other axes.

The contribution that each unit area has to the area moment of inertia scales quadratically with distance from the bending axis.

For any shape, the moment of inertia about an axis is 
$$
I=\int{y^2}\;dA
$$
where y is the perpendicular distance from the axis to the area element dA and dA is a very small element of the shape's area.

| SHAPE     | $I_x$               | $I_y$               |
| --------- | ------------------- | ------------------- |
| Rectangle | $\frac{bh^3}{12}$   | $\frac{hb^3}{12}$   |
| Circle    | $\frac{\pi r^4}{4}$ | $\frac{\pi r^4}{4}$ |

### Parallel Axis Theorem
The parallel axis theorem states that to find the area moment of inertia for any axis from the area moment of inertia for the centroidal axis, you can use the following formula
$$
I=I_{centroid}+Ad^2
$$
Where $I_{centroid}$ is the area moment of inertia for the axis running through the centroid of the shape, $A$ is the area of the shape, and $d$ is the distance between the new axis of interest and the axis running through the centroid.

## Neutral Axis
When a beam is under a load, it has a tendency to bend. As long as this bending remains in the elastic region of deformation (no permanent deformation), we can study it's deformation. The bending moment in a body describes how much bending is being applied to the body or how strong its tendency to bend will be. 

If a beam is loaded from the top, the bending that occurs in a beam will cause fibres along the top of the beam to compress and get shorter and fibres on the bottom of the beam to elongate. We say that the top of the beam is in compression and the bottom of the beam is in tension.

The further a fibre is from some central point in the beam, the more it will be in either tension or compression. This means that at some point in the centre, the fibre will be in neither tension nor compression. This axis runs through the beam and is called the neutral axis, defined as the axis through which the beam does not change length under loading. The centroidal axis of a cross section is not necessarily the same as the neutral axis.

## Double Integration
A useful property to know about a beam under a load is how much it will deflect or move away from its initial position throughout the beam due to the load. Since we know the equation for the curvature of a beam and we know that the curvature of a beam is the second derivative of the deflection of the beam, we can find an equation for the deflection of the beam as

$$
y=\int \int \frac{M(x)}{EI}\;dx\;dx
$$
This is called the Double Integration Method for finding the deflection of beams under loading. By convention, positive values for $y$, imply the beam will deflect downwards under loading.

### Example
![[Screenshot 2024-12-26 at 06.25.34.png]]
For a simply supported beam (one pin and one roller support) with a single point load in the centre, we can split the beam into two sections, each with a different bending moment equation.

To calculate the bending moment for this general case, we must first calculate the reaction forces at the supports. The leftmost (pin) support will have two reaction forces, a horizontal force $A_x$ and a vertical force $A_y$. The rightmost (roller) support will only have a vertical reaction $B_y$. We also have a vertical force acting downwards which we'll call $P$. 

Using our 3 equilibrium equations and taking the length of the beam to be $L$:
Horizontal Forces
$$
\sum{F_x}=0\hspace{0.5cm}\therefore A_x=0
$$
Vertical Forces
$$
\sum{F_y}=0\hspace{0.5cm}\therefore A_y+B_y=P
$$
Bending Moments About A
$$
\sum{M_A}=0\hspace{0.5cm}\therefore -\frac{PL}{2}+ByL=0
$$
We can solve for $B_y$ using the bending moment equilibrium equation.
$$
B_y=\frac{P}{2}
$$
and then using the vertical force equilibrium equation
$$
A_y=P-\frac{P}{2}=\frac{P}{2}
$$
This passes the sanity check as it tells us that the force $P$ acts the same amount on both supports. 

Now we can find the bending moment in each section of the beam using the method of sections.

For $0 \leq x \leq \frac{L}{2}$
$$
M_1(x)=\frac{Px}{2}
$$
For the rightmost section, we need to take into account the bending moment created as a reaction to both the point load $P$ and the reaction $A_y$
For $\frac{L}{2} \leq x \leq L$
$$
M_2(x)=\frac{Px}{2}-P\left(x-\frac{L}{2}\right)
$$
With these two sections, we can now find the deflection for each point by integrating each equation, divided by the flexural rigidity ($EI$), twice.

Note that after a single integration, we have the equation for the slope of a beam at any point throughout its length.
$$
\begin{align}
\theta_1&=\int \frac{Px}{2EI}\;dx&=\frac{Px^2}{4EI}+c_1\\
y_1&=\int \frac{Px^2}{4EI}+c_1\;dx&=\frac{Px^3}{12EI}+c_1x+c_2
\end{align}
$$
And for the rightmost section we'll start by rearranging the equation slightly:
$$
\begin{align}
\frac{d^2y}{dx^2}&=\frac{Px}{2EI}-\frac{P\left(x-\frac{L}{2}\right)}{EI}\\
&=\frac{Px}{2EI}-\frac{Px}{EI}+\frac{PL}{2EI}
\end{align}
$$
Then:
$$
\begin{align}
\theta_2&=\int \frac{Px}{2EI}-\frac{Px}{EI}+\frac{PL}{2EI}\;dx&=\frac{Px^2}{4EI}-\frac{Px^2}{2EI}+\frac{PLx}{2EI}+c_3\\
y_2&=\int \frac{Px^2}{4EI}-\frac{Px^2}{2EI}+\frac{PLx}{2EI}+c_3\;dx&=\frac{Px^3}{12EI}-\frac{Px^3}{4EI}+\frac{PLx^2}{4EI}+c_3x+c_4
\end{align}
$$
When a beam deflects, the deflection, slope, and curvature should all remain continuous along its length. Otherwise the beam would have a break in it. Therefore, where the two sections connect, we should expect the slope and deflection to have the same value. In this case, this occurs at $x=\frac{L}{2}$. This can be used to solve for $c_2$ and $c_4$.

However, there are two interesting properties of this beam which can make solving for the constants easier. Firstly, note that $c_2$ and $c_4$ represent the initial and find deflections of the beam or the deflections of the extents of the beam. Since we know the beam is unable to deflect at its extents, we can say that $c_2=c_4=0$.

Secondly, the slope of the beam under the point load (at the centre) must be 0 and this will also be where the maximum deflection occurs.

Therefore we can say
$$
\begin{align}
\theta_1\left(\frac{L}{2}\right)&=0\\
\frac{PL^2}{16EI}+c_1&=0\\
c_1&=-\frac{PL^2}{16EI}
\end{align}
$$
and also
$$
\begin{align}
\theta_2\left(\frac{L}{2}\right)&=0\\
\frac{PL^2}{16EI}-\frac{PL^2}{8EI}+\frac{PL^2}{4EI}+c_3&=0\\
c_3&=\frac{3PL^2}{16EI}
\end{align}
$$
Therefore, the deflection of the beam in each section is given by
$$
\begin{align}
y_1(x)&=\frac{Px^3}{12EI}-\frac{PL^2x}{16EI}\\
y_2(x)&=\frac{Px^3}{12EI}-\frac{Px^2}{4EI}+\frac{3PL^2x}{16EI}
\end{align}
$$
## Macaulay's Method
While the previously described Double Integration Method yields the correct result, it can be complicated and messy for anything but a simple case. Macaulay's Method simplifies the calculation by using the Heaviside function to combine sections of a beam with different bending moments into a single, integrable function. This can then be integrated twice much more simply to yield the correct deflection equation.

### The Heaviside Function
The Heaviside or Step Function allows sections of a function to be turned on or off depending on the value of the input. If the value of the input is negative, the entire function falls to 0, otherwise it goes 1. 
A more rigorous mathematical description is
$$
H(x)=
\begin{cases}
0 & x<0\\
1 & x\geq 0
\end{cases}
$$

### Macaulay Brackets
Macaulay takes the Heaviside function a little further and says that the function should still go to 0 is the input is negative but should go to the value of the input if the input is positive. It is denoted using angle brackets. For example $\langle 2x \rangle$ would yield $4$ when $x=2$ and $0$ when $x=-3$ or more generally when $x \leq 0$
$$
\langle x \rangle=
\begin{cases}
0 & x<0\\
x & x\geq 0
\end{cases}
$$
Integration of a Macaulay bracket can be achieved by using the power rule. 
$$
\int \langle x-a \rangle^n = \frac{1}{n+1}\langle x-a \rangle^{n+1}
$$
This is a very simple integration and allows solutions to be reached considerably faster than with the double integration method.
### Piecing It Together
Taking the previous example, we can use Macaulay brackets to make the calculation much simpler. We'll start back with the bending moment equation we found for each section of the beam.

$$
\begin{align}
M_1(x)&=\frac{P}{2}x\\
M_2(x)&=\frac{P}{2}x-P\left(x-\frac{L}{2}\right)
\end{align}
$$
 
 The first thing to note is that the $\frac{P}{2}x$ section is common to both sections of the beam and can be left unchanged. The second section has an additional term which must only apply for values of $x$ such that $\frac{L}{2} \leq x$ (the upper bound of $L$ is assumed and not strictly needed here.) If we replace the existing brackets with Macaulay brackets, the result is exactly what we're after
$$
M(x)=\frac{P}{2}x - P \left \langle x - \frac{L}{2} \right \rangle
$$
In this case, only when $x$ is greater than half the length of the beam $L$ will the second term be activated. Otherwise, the entire second term falls to $0$.

Now we can integrate the equation twice.
$$
\frac{d^2y}{dx^2}=\frac{1}{EI}\left(\frac{P}{2}x - P \left \langle x - \frac{L}{2} \right \rangle\right)
$$
Therefore
$$
\begin{align}
\theta(x)&=\frac{1}{EI}\int\frac{P}{2}x - P \left \langle x - \frac{L}{2} \right \rangle dx = \frac{1}{EI}\left(\frac{Px^2}{4}-\frac{P}{2}\left \langle x-\frac{L}{2} \right \rangle^2\right)+c_1\\
y(x)&=\frac{1}{EI}\int\theta(x)dx=\frac{1}{EI}\left(\frac{Px^3}{12EI}-\frac{P}{6}\left \langle x-\frac{L}{2} \right \rangle^3\right)+c_1x+c_2
\end{align}
$$
 We can use this to solve for $c_1$ and $c_2$, and calculate $\theta_{max}$ and $y_{max}$. 
## Superposition

## BMDs

# Stress Transformation
## Mohr's Circle


# Torsion

# Buckling