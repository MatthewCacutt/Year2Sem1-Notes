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

## Projectiles

## Curvilinear Motion

## Absolute Dependent & Relative Motion

# Kinetics

## Work & Energy

## Conservation of Energy



