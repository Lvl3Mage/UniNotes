## Center of Mass (CoM/CM)
The average position of all masses in a system (weighed towards bigger masses)

`.img--75, center`![[CoMOf2Blocks|100%]]

$$CoM = \frac{\sum^{n}_{i=1} m_{i}\overrightarrow{pos_{i}}}{\sum^{n}_{i=1}m_{i}}	$$

> [!info] 
> Add all the positions together, scaling (multiplying) them by their masses and devide the total sum by the total mass 

Exercise 1 [[Physics Unit 4 Exercises#Ex1]]

### Objects with holes
For objects that have holes of a specific shape for which calculating the CoM is possible), we can treat these holes as objects with **negative mass** during CoM calculation. 

1. Forget about the holes and calculate the CoM for the main object.
2. When calculating the final CoM add the holes as objects with negative mass.

Exercise 2 [[Physics Unit 4 Exercises#Ex2]]

### CoM Velocity and acceleration calculation
When calculating the velocity or acceleration the same equation can be applied:

$$CoM = \frac{\sum^{n}_{i=1} m_{i}\overrightarrow{v_{i}}}{\sum^{n}_{i=1}m_{i}}	$$

$$CoM = \frac{\sum^{n}_{i=1} m_{i}\overrightarrow{a_{i}}}{\sum^{n}_{i=1}m_{i}}	$$

> [!info] 
> Only forces that are external to the system (a force pushing on to one of the objects for example) can affect the velocity/acceleration of CoM. No change/Force from inside the system can change that value


## Angular inertia
A value that acts against the object's angular acceleration. It essentially has the same meaning as the mass of the object in linear acceleration.

> [!important] 
> There are as many possible inertias as there are axes of rotation

### Single point mass
$$I_{desc} = m*r^2$$
> [!note] 
> For a point mass rotating around a point in space

#todo Add diagram of point mass rotating around point in space

### Multiple point masses
$$I_{desc} = \sum^{n}_{i = 1}m_i*r_i^2$$
> [!note] 
> For multiple point masses rotating around a point in space

### Continous masses
$$I_{cont} = \int r^2 dm$$
#### Linear
$$\rho_l = \frac{dm}{dl} \rightarrow dm = \rho_l * dl (\frac{kg}{m})$$
#### Surface
$$\rho_s = \frac{dm}{ds} \rightarrow dm = \rho_s * ds (\frac{kg}{m^2})$$
#### Volumetric
$$\rho_v = \frac{dm}{dv} \rightarrow dm = \rho_v * dv (\frac{kg}{m^3})$$
### Parrallel axis theorem
If we know the angular inertia of an object through an axis that passes through the object's center of mass, we can calculate the intertia through a different axis that is parrallel to the original one using this formula:
$$I = I_{cm} + md^2$$
`.img--50, center`![[Parrallel-axis.excalidraw|100%]]``
### Forces
>[!info] 
>Any angular acceleration around the center of rotation is produced by a force located at a point that is different from the center of rotation

$$\overrightarrow{\tau} = \overrightarrow{r} \times \overrightarrow{F}$$
$$|\overrightarrow{\tau}| = |\overrightarrow{r}|*|\overrightarrow{F}|*\sin{\theta}$$
`.img--50, center`![[AngularMomentumForces.excalidraw|100%]]
In this case torque is represented by a vector that is perpendicular to both the force vector and the radius vector. It can be calculated as the cross product between the 2 vectors.

The radius vector in this case is calulated as the shortest vector between the point the force is applied to and the axis of rotation.

>[!tip] 
>In this case torque can be thought as an equivalent of force in the world of rotational motion. 

The torque can then be used to calculalte the angular acceleration using the inertia on the axis of rotation
$$\tau = I * \alpha$$

#todo Finish notes cuz I'm lazy rn

### Rolling motion without sliding

When talking about an object that presents this type of movement we can assume that any point on it presets a velocity that can be expressed as a sum of 2 vectors. One vector being the object's COM velocity and the other being the rotational velocity of that point. The following diagram demonstrates this in an intuitive way:

![[Pasted image 20230512093952.png|500]]








