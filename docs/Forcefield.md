## FORCE FIELD EQUATION
We have studied in the previous section that, to obtain trajectory we need to solve Newtons equation of motion. 
### How to obtain the solve Newton;s equaion of motion and obtain force? 
The force is obtained differentiating Potential energy term which is given by the following equation,
<!--- ![image](https://github.com/user-attachments/assets/2cece935-4376-42e3-a44b-29db24e8c323)--->
<img src="https://github.com/user-attachments/assets/2cece935-4376-42e3-a44b-29db24e8c323" alt="Image Description" width="600">

Here, in MD simulations we assume atoms as hard spheres with charge **q** and springs are attached between two atoms with a force constant **K**. The potential energy at time t is obtained by the above equation. Upon solving the above equation for time (t+ $\delta t$), we can get new forces at time (t+ $\delta t$)




### Algoritham To Solve Newtons equation of Motion
- Verlet Algoritham
- Velocity Verlet Algoritham
- Leap frog Algoritham

### Verlet Algoritham
From what we saw until now, it is clear that to retrieve the trajectory of a molecule one has to be able to integrate the equations of motion. However, we did not specify how this is achieved in practice yet.
To understand the mechanisms behind this procedure we first need to underline a concept that is central to nearly all the algorithms we use to obtain molecular motion. The majority of these techniques are assumed to be valid because the position, as well as the dynamical properties of a molecule at time $t+\delta t$, can be approximated through a Taylor expansion at time $t$.

 
$$r(t+\delta t) = r(t) + \delta t v(t) + \frac{1}{2} \delta t^2 a(t) + \frac{1}{6} \delta t^3 b(t) + \dots$$


$$v(t+\delta t) = v(t) + \delta t a(t) + \frac{1}{2} \delta t^2 b(t) + \dots \$$


$$a(t+\delta t) = a(t) + \delta t b(t) + \dots$$
 
where $v$ is the velocity, $a$ the acceleration, $b$ is the third derivative of the position with respect to time, and so on. This approximation gets better when the $\delta t$ is smaller.
As already stated, there are many algorithms to integrate Newton’s equation, providing a simulation of the motion of a molecule. The most widely used is a used is a  numerical method named the Verlet algorithm.

The latter uses the current positions $r(t)$ and accelerations $a(t)$, and the positions from the previous step $r(t - \delta t$) to retrieve the positions in the following step $r(t+\delta t$). The algorithm originates by simply writing the equations for the past and future positions:
 
$$\mathbf{r}(t+\delta t) = \mathbf{r}(t) + \delta t \mathbf{v}(t) + \frac{1}{2} \delta t^2 \mathbf{a}(t) +  \dots$$

$$\mathbf{r}(t-\delta t) = \mathbf{r}(t) - \delta t \mathbf{v}(t) + \frac{1}{2} \delta t^2 \mathbf{a}(t) + \dots$$

and adding these two terms we have that:
 
$$r(t + \delta t) = 2r(t) - r(t- \delta t) + \delta t^2 a(t)$$

which is the basic Verlet algorithm equation.
According to this principle, if we want to know the position of an atom in the future $r(t + \delta t)$ we need the position in the present $r(t)$ and in the past $r(t- \delta t)$ plus the present acceleration $a(t)$.



**References**
1. https://www.compchems.com/molecular-dynamics-equations-of-motion/#the-verlet-algorithm




