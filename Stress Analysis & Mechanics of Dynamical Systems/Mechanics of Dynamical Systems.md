# Kinematics vs Kinetics
Kinematics is the study of the motion of particles using their position, velocity, and acceleration at a given instant. Kinetics is the study of the motion of particles using the forces involved in its motion.
# Kinematics
## Rectilinear Motion
Rectilinear motion describes motion in straight lines in one dimension. The position of a particle in rectilinear motion is defined using a single coordinate axis $s$ with a fixed origin point $O$. The position of the particle is defined relative to the origin point with positions one side of the origin being negative and the other being positive though this is determined by the scenario. 

The displacement of a particle is defined as the change in its position
$\Delta s=s'-s$
where $s'$ is the final position of the particle and $s$ is the initial position. The displacement of a particle is distinct from its distance in that the distance travelled takes into account the total length of the path travelled while the displacement only describes the distance between a starting and ending point. 

When a particle moves through some displacement $\Delta s$ over time interval $\Delta t$, the average velocity of the particle is
$$v_{avg}=\frac{\Delta s}{\Delta t}$$
Over an infinitesimally small time interval, the displacement will also be infinitesimally small leading to an instantaneous velocity of
$$
v=\frac{ds}{dt}
$$
Given that a change in time will only ever be positive, the sign of the displacement will be equal to that of the velocity. If a particle moves in the negative direction, it will have negative velocity.

When a particle moves between two known velocities $\Delta v$ over time interval $\Delta t$, the average acceleration of the particle is
$$
a_{avg}=\frac{\Delta v}{\Delta t}
$$
Over an infinitesimally small time interval, the change in velocity will also be infinitesimally small leading to an instantaneous acceleration of
$$
a=\frac{dv}{dt}
$$
Therefore,
$$
a=\frac{d^2s}{dt^2}
$$
The sign of the acceleration of a particle does not indicate its direction of motion. A sign for $a$ which is opposite to the direction of motion of the velocities indicates deceleration.

By eliminating the time differential dt, we find
$$
dt=\frac{dv}{a}=\frac{ds}{v}
$$
Therefore
$$
v\;dv=a\;ds
$$
Under a constant acceleration $a=a_c$, each of the equations derived above can be integrated to give three new equations.
#### Velocity as a Function of Time
Integrating
$$
a_c=\frac{dv}{dt}
$$
gives

$$
\begin{align}
\int_{v_0}^v \; dv &= \int_0^t a_c dt\\
v-v_0&=a_ct\\
\end{align}
$$
Therefore
$$
v=v_0+a_ct
$$
#### Position as a Function of Time
Integrating $$v=\frac{ds}{dt}=v_0+a_ct$$
gives
$$
\begin{align}
\int_{s_0}^s \; ds &= \int_0^t v_0+a_ct \; dt \\
s-s_0&=v_0t+\frac{1}{2}a_ct^2
\end{align}
$$
Therefore
$$
s=s_0+v_0t+\frac{1}{2}a_ct^2
$$

#### Velocity as a Function of Position
Starting with
$$
v=v_0+a_ct
$$
Squaring both sides leads to
$$
\begin{align}
v^2&=v_0^2+2v_0a_ct+a_c^2t^2\\
v^2&=v_0^2+2a_c\left(v_0t+\frac{1}{2}a_ct^2\right)
\end{align}
$$
The terms inside the bracket make up a simpler equation for displacement where $s_0$ is assumed to be $0$. Therefore we can simply subtract off $s_0$ to give
$$
v^2=v_0^2+2a_c(s-s_0)
$$

#### Erratic Motion
When the motion of a particle is erratic, its position, velocity, and acceleration will need to be described by a series of functions. For this reason, graphs are useful in describing motion.
The slope of a s-t graph is the velocity of the particle over time.
The slope of a v-t graph is the acceleration of the particle over time.
The area under an a-t graph gives the velocity over time.
The area under a v-t graph gives displacement over time.
## Curvilinear Motion
Curvilinear motion occurs when a particle moves along a curved path. This is often in three dimensions.

The position of a particle on a space curve defined by s(t) can be measured from a fixed point $O$ and represented by a position vector $\mathbf{r}(t)$. When the particle moves along the curve s(t) by some amount $\Delta s$, it has a new position such that $\Delta \bf{r} = \bf{r}' - \bf{r}$. The change in position $\Delta \bf{r}$ is the displacement of the particle found using vector subtraction.

Note that $s$ represents the arc length and when the position of the particle changes, its straight line displacement $\mathbf{r}$ will always be shorter than the distance travelled along the curve $s$. In essence, $\mathbf{r}$ forms the chord of $s$.

If $\Delta \bf{r}$ occurs over a time interval $\Delta t$, the average velocity of the particle is
$$
\mathbf{v}_{avg}=\frac{\Delta\mathbf{r}}{\Delta t}
$$
Note that in this case $\mathbf{v}_{avg}$ is also a vector. The instantaneous velocity is given by
$$
\mathbf{v}=\frac{d\mathbf{r}}{dt}
$$
Because we are taking the limit as the distance between two points on a curve goes to zero, the direction of the velocity vector will be tangent to the curve. Over a small enough time interval, the change in displacement and change in distance along the curve are indistinguishable besides the direction included in the displacement vector. Therefore speed can be obtained by
$$
v=\frac{ds}{dt}=\frac{|d\mathbf{r}|}{dt}
$$
A change in velocity $\mathbf{v}$ between two points in time such that $\Delta\mathbf{v}=\mathbf{v}'-\mathbf{v}$ can yield an average acceleration by
$$
\mathbf{a}_{avg}=\frac{\Delta\mathbf{v}}{\Delta t}
$$
Note that in this case $\mathbf{a}_{avg}$ is also a vector. As the time between a change in velocity goes to zero, we obtain the instantaneous acceleration
$$
\mathbf{a}=\frac{d\mathbf{v}}{dt}
$$
Alternatively
$$
\mathbf{a}=\frac{d^2\mathbf{r}}{dt^2}
$$
By placing the velocity vectors as arrows on the fixed point $O$, and extending them to points on the curve we create a *hodograph*. An acceleration vector typically acts tangent to the hodograph and is not tangent to the path of motion.

### Rectangular Components
Particles can also be described along a path by $x$, $y$, and $z$ components such that
$$
\mathbf{r}=x\mathbf{i}+y\mathbf{j}+z\mathbf{k}
$$
When the particle moves, each component will be a function of time such that $x=x(t)$, $y=y(t)$, and $z=z(t)$ leading to $\mathbf{r}=\mathbf{r}(t)$.
The magnitude of the position vector can be found using the Pythagorean theorem.
$$
r=\sqrt{x^2+y^2+z^2}
$$
The direction of $\mathbf{r}$ is given by the unit vector $$\mathbf{u}_r=\mathbf{\hat{r}}=\frac{\mathbf{r}}{r}$$
The time derivative of the position vector yield the velocity. Hence, by the sum rule of calculus,
$$
\mathbf{v}=\frac{d\mathbf{r}}{dt}=\frac{d}{dt}x\mathbf{i}+\frac{d}{dt}y\mathbf{j}+\frac{d}{dt}z\mathbf{k}
$$
Here, the product rule must be used
$$
\frac{d}{dt}x\mathbf{i}=\frac{dx}{dt}\mathbf{i}+\frac{d\mathbf{i}}{dt}x
$$
But since $\mathbf{i}$ does not change with time, $\frac{d\mathbf{i}}{dt}=0$
Leading to
$$
\mathbf{v}=\frac{dx}{dt}\mathbf{i}+\frac{dy}{dt}\mathbf{j}+\frac{dz}{dt}\mathbf{k}
$$
And since the derivative of the $x$ position function is the $x$ velocity function and so on,
$$
\mathbf{v}=v_x\mathbf{i}+v_y\mathbf{j}+v_z\mathbf{k}
$$
The velocity vector has a magnitude given by the Pythagorean theorem
$$
v=\sqrt{v_x^2+v_y^2+v_z^2}
$$
and a direction given by the unit vector
$$
u_\mathbf{v}=\mathbf{\hat{v}}=\frac{\mathbf{v}}{v}
$$
which is always tangent to the path of motion.

Likewise, the acceleration of a particle is obtained by taking the time derivative of the velocity leading to
$$
\mathbf{a}=\frac{d\mathbf{v}}{dt}=a_x\mathbf{i}+a_y\mathbf{j}+a_z\mathbf{k}
$$
where
$$
\begin{align}
a_n=\frac{dv_n}{dt}=\frac{d^2n}{dt^2}
\end{align}
$$
for each component.
The acceleration of the particle has a magnitude given by the Pythagorean theorem
$$
a=\sqrt{a_x^2+a_y^2+a_z^2}
$$
and a direction given by the unit vector
$$
u_\mathbf{a}=\mathbf{\hat{a}}=\frac{\mathbf{a}}{a}
$$
which is not tangent to the path of motion.
### Normal & Tangential Components
For a known path, the motion of a particle can be described using two axes, one which is normal to the path and one which is tangent to the path.

For a particle at position $s$ along a curve measure from point $O$ the $t$ axis is tangent to the curve at the particle and positive in the direction of increasing $s$. The positive direction has unit vector $\mathbf{u}_t$. The path of motion can be segmented into infinitesimally small segments of length $ds$ whereby each segment is the arc of a circle with radius of curvature $\rho$ and centre of curvature $O'$. The normal axis is perpendicular to the tangential axis and positive in the direction towards the centre of curvature for the segment on which the particle lies. In effect, the direction of the positive normal vector is always on the concave side of the curve of motion with unit vector $\mathbf{u}_n$.

### Cylindrical Components

### Projectile Motion
When examining free flight motion of projectiles with rectangular components, by neglecting air resistance, only the weight of the projectile causes an acceleration. This acceleration is due to gravity and acts only in the downwards vertical direction meaning by splitting the components of the velocity vectors, the horizontal component(s) have a constant acceleration of 0 meaning they also have a constant velocity, and the vertical component has a constant acceleration of $a_y=g=9.81m/s^2$ downwards.

The equations of motion are therefore modified
Under horizontal motion:
$$
\begin{align}
v&=v_0+a_ct &\hspace{0.5cm} v_x&=v_{0_x}\\
x&=x_0+v_0t+\frac{1}{2}a_ct^2 &\hspace{0.5cm} x&=x_0+v_{0_x}t\\
v^2&=v_0^2+2a_c(x-x_0) &\hspace{0.5cm} v&=v_{0_x}
\end{align}
$$
Under vertical motion:
$$
\begin{align}
v&=v_0+a_ct &\hspace{0.5cm} v_y&=v_{0_y}-gt\\
y&=y_0+v_0t+\frac{1}{2}a_ct^2 &\hspace{0.5cm} y&=y_0+v_{0_y}t-\frac{1}{2}gt^2\\
v^2&=v_0^2+2a_c(y-y_0) &\hspace{0.5cm} v^2&=v_{0_x}^2-2g(y-y_0)
\end{align}
$$

## Absolute Dependent & Relative Motion
### Analysis of Two Particles
## Translating Axes


# Kinetics

## Work & Energy

## Conservation of Energy



