# Polarization and Stokes Parameters

<h4>Author of this code:</h4>

- Javier Alejandro Pérez Garza

## Code Explanation

In this code the first graph is of a Gaussian beam that is written in the following way:

$$\vec{E}(R,\phi) = \left(\frac{R}{\omega_0}\right)^{|m|} e^{-\left(\frac{R}{\omega_0}\right)^2\} e^{i m \phi}.$$

In Jones formalism, the field is written as,

$$
\vec{E}(z, t)= 
\begin{bmatrix}
E_{0x} e^{i\phi_x} \\
E_{0y} e^{i\phi_y}
\end{bmatrix}.
$$

This way, we can associate different polarization states to the field. For example, for a vertical polarization of the field, the Jones vector is:

$$
| V \rangle=
\begin{bmatrix}
0 \\
1
\end{bmatrix}.
$$

Using this notation, with the Jones matrix we can obtain the emerging light beam of different optical devices using the following equation:

$$E_{out}=JE_{in}.$$

In this code I use a polarizer, a QWR, and a HWR. Their Jones matrix are as follow:

$$
J_p(\theta) =\begin{bmatrix} \cos^2 \theta  & \sin \theta \cos \theta \\
\sin \theta \cos \theta &\sin^2 \theta\end{bmatrix}, 
$$

$$
J_{\lambda/2}(\theta) =\begin{bmatrix} \cos 2 \theta  & \sin 2 \theta  \\ 
\sin 2\theta  &-\cos 2 \theta\end{bmatrix}, 
$$

$$
J_{\lambda/4}(\theta) =\frac{1}{\sqrt{2}}\begin{bmatrix} 1-i\cos 2 \theta  & -i\sin 2 \theta  \\ 
-i\sin 2\theta  &1+i\cos 2 \theta\end{bmatrix}.
$$

For the experimental polarization state different experimental arrays were made so that I could get the Stokes parameters. They are defined as:
- $S_0 = I,$
- $S_1 = Q,$
- $S_2 = U,$
- $S_3 = V.$

so that,

$$
\begin{aligned}
S_0 &= |E_x|^2 + |E_y|^2 \\
S_1 &= |E_x|^2 - |E_y|^2 \\
S_2 &= 2 \text{Re}(\{ E_x E_y^* \}) = |E_u|^2 - |E_v|^2 \\
S_3 &= 2 \text{Im}(\{ E_x E_y^* \}) = |E_R|^2 - |E_L|^2
\end{aligned}.
$$

_Note:_ $S_3$ is a different V than the vertical Jones vector.

The Stokes parameters are often combined into a vector, known as the Stokes vector:

$$
\vec{S} = \begin{bmatrix}
S_0 \\
S_1 \\
S_2 \\
S_3
\end{bmatrix}.
$$

With this parameters the degree of polarization can be calculated: 

$$
p=\frac{\sqrt{S_1^2+S_2^2+S_3^2}}{S_0}.
$$

Finally, using Stokes parameters we can graph the electric field in terms of the polarization ellipse. First we define the complex intensity of linear polarization $L= Q+iU$, then taking the absolute value $|L|=\sqrt{Q^2+U^2}$. Finally we can calculate the parameters of the polarization ellipse:

- $A=\sqrt{\frac{1}{2}(I+|L|)},$
- $B=\sqrt{\frac{1}{2}(I-|L|)},$
- $\theta = \frac{1}{2} \arctan \left(\frac{U}{Q}\right).$





