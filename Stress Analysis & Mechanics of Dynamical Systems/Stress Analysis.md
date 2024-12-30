# Definitions & Equations

***Stress*** is a measure of the amount of pressure or force exerted on a body or material. 

***Normal Stress*** refers to the stress due to axial loading either compressive or tensile. It is denoted by $\sigma$ and calculated by dividing the force or pressure exerted by an axial load by the cross sectional area.
$$
\sigma=\frac{P}{A}
$$
It is positive when the stress is tensile and negative when it is compressive and has units of $Pa$(scals) or $N/m^2$. Engineering stress uses the original area of a cross section for deformation to simplify calculations despite the cross section having a malleable size due to strain.

***Axial Loads*** are forces applied parallel to the main axis and normal to the surface of a material. For a rod, this is the axis running through the centre longitudinally.

***Strain*** is a measure of the amount of deformation to a body as a result of stress. 

***Normal Strain*** is a measure of a deformation to a body due to *normal stress*. It is denoted by epsilon $\epsilon$, and given by the equation:
$$
\epsilon=\frac{\delta}{L}
$$
Where $\delta$ is the change in length, and $L$ is the original length of the material. 

***Young's (Elastic) Modulus*** is a material property which defines the ratio between normal material stress and strain within the elastic region of deformation. It is represented by the letter $E$ and given by equation
$$
E=\frac{\sigma}{\epsilon}
$$

***Yield Strength*** is the stress required for a material to enter the plastic region.

***Ultimate Strength*** is the highest value for stress on the stress strain curve.

***Shear Stress*** refers to stress which run parallel to the cross section of a body. 
- Direct Shear happens when two parts of a single member are subjected to forces or loads in opposite directions (non-axially). This causes a shear stress of the load force divided by the cross sectional area (V is used for shear loads)
$$
\text{Direct Shear}=\tau=\frac{V}{A}
$$

***Shearing Strain*** is the amount by which a body rotates due to shearing stress. 

***Shear Modulus (of Rigidity)*** is the ratio between shear stress and shear strain under elastic deformation such that
$$
G=\frac{\tau}{\gamma}
$$

***Axial Deformation*** $\delta$ is the change in length $L$ of a material with cross section $A$ and Young's modulus $E$ due to axial loading $P$ such that
$$
\delta=\frac{PL}{AE}
$$

***Coefficient of Thermal Expansion*** is a material property which measures how sensitive a material is to deformation caused by temperature change. It is represented by $\alpha$ and used to find the change $\delta$ in length of a material $L$ due to a temperature change $\Delta T$.
$$
\delta = \alpha \cdot \Delta T \cdot L
$$

***Total Axial Deformation*** is the total amount a member will elongate or shorten axially as a result of both temperature change and axial loads. It is given by
$$
\delta_{\text{Total}}=\alpha L \Delta T + \frac{PL}{AE}
$$
***Poisson's Ratio*** is a material property measuring how much a material deforms laterally as a result of axial, longitudinal strain. 
$$
\nu=\frac{\epsilon_{\text{lateral}}}{\epsilon_{\text{longitudinal}}}
$$
It usually has values between 0 and 0.5.

***Statically Indeterminate Problems*** are problems where the equilibrium equations are not enough to find reaction or internal forces required for solving problems. 

***Stress Concentration Factor*** is a property governed by the shape and material of a body. It describes the ratio between maximum stress and average stress such that
$$
K=\frac{\sigma_{\text{max}}}{\sigma}
$$
Therefore, the maximum stress for a body under the four main types of stress deformation (bending, buckling, torsion, and shear) can be calculated by multiplying the stress concentration factor by the equation for the average stress such as $\sigma_{\text{max}}=K\frac{P}{A}$ for axial loading.

***Maximum Allowable Stress*** is the maximum stress within a member without causing it to fail. 

***Factor of Safety*** is a value quantifying how safe a member is under current stress. It is defined as the ratio of the maximum allowable stress to the maximum current stress such that
$$
n=\frac{\sigma_{\text{allowable}}}{\sigma_{\text{max}}}
$$
The higher the factor of safety, the less likely the member is to fail. A FoS of less than 1 means the member will fail under the stress used in the formula.

# Deflection of Beams (Bending)
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
The principle of superposition states that for any complex loading system made up of multiple distributed and/or point loads, the deflection that the beam undergoes is equal to the sum of the deflection of its parts.

This means that if a beam has a single UDL (uniformly distributed load) and a single point load, the deflection of the beam will be the sum of the deflection of a beam with only the UDL and a beam with only the point load. This helps to find much more complicated deflection patterns using common deflection equations.
# Stress Transformation (Shearing)
When stress is caused by coplanar loadings, the 3D stress state element can be analysed using a single plane of the stress element consisting of an $x$ and $y$ normal stress and four shear stresses forming a single shear stress component $\tau_{xy}$ which acts on each of the four faces of the planar element.
![[Screenshot 2024-12-27 at 16.23.25.png]]
The orientation of the stress element itself will affect these stresses. Any stress state is comprised of three stresses: two normal stresses ($\sigma_x$ and $\sigma_y$) and a shear stress component ($\tau_{xy}$) in a specific orientation given by an angle $\theta$.

## Mohr's Circle


# Twisting (Torsion)

# Columns (Buckling)
When a long and slender member is under axial compressive loading (column), it may suddenly deflect laterally (buckling). A buckling column often leads to failure of structure. The maximum axial load a column supports on the verge of buckling is the critical load $P_{cr}$. Any extra load will cause buckling. 