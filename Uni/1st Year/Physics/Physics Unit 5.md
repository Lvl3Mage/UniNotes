## Work
#### Static forces
Work is defined as the product between a force and the distance that the force made an object move. 
`.img--50, center`![[Work.excalidraw|100%]]

$$W = \overrightarrow{F} \cdot \overrightarrow{s}$$
>[!tip] 
>This basically just means that a force that doesn't move an object doesn't do any work. The implication of the dot product is that if the movement of the object is perpendicular to the force then the force must have not had any effect on that movement and thus the work is 0.

#### Varying forces
When a force changes during the movement we must integrate it with respect to displacement.
The general formula is:

$$W = \int_{x_1}^{x_2} F dx$$
>[!info]
>This is because the original formula depends on both the force and the position change.
>Since the force varies, we need to break the displacement into small increments, and calculate the work done by the force over each increment. The smaller the increments, the more accurately we can calculate the work done by the force. 
>
>We can then sum up the work done over all the increments to find the total work done by the force over the entire displacement. This is effectively what an integral does - it sums up infinitesimally small increments of a function over a given interval.

>[!example] 
>The easiest way to apply this formula is when the force directly depends on position (for examplle in a spring). When the force depends on some other variable like time we need to try and express it in terms of position instead and use that in the integral.



## Energy
The kinetic energy formula is defined as:
$$E_c = \frac{1}{2}mv^2$$
>[!note] 
If you calculate the work formula along the tangent axis of the movement of an object you will get that work can be defined as:
$$W_{ab} = \frac{1}{2}mv_b^2 - \frac{1}{2}mv_a^2$$
This means that work can be also defined as the change in the kinetic energy of an object.

When an object also posses a rotational motion it must be included in the calculation of the kinetic energy:
$$E_c = E_{trans} + E_{rot} = \frac{1}{2}mv^2 + \frac{1}{2}I\omega^2$$
## Power
In physics power is defined as work done per unit of time. Power is defined by the following equation:
$$P = \frac{dW}{dt}$$
#### Instantaneous power
###### Translation work
$$P = \frac{dW}{dt} = \frac{ \overrightarrow{F}\cdot d\overrightarrow{x}}{dt} = \overrightarrow{F} \cdot \overrightarrow{v}$$
###### Rotation work
$$P = \frac{dW}{dt} = \frac{ \overrightarrow{\tau}\cdot d\overrightarrow{\theta}}{dt} = \overrightarrow{\tau} \cdot \overrightarrow{\omega}$$

