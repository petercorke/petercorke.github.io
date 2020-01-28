---
layout: default
parent: TOC_differential
---
# trlog
_Logarithm of SO(3) or SE(3) matrix_


```S = trlog(R)``` is the matrix logarithm (3&times;3) of `R` (3&times;3) which is a skew
symmetric matrix corresponding to the vector theta*w where theta is the
rotation angle and w (3&times;1) is a unit-vector indicating the rotation axis.


```[theta,w] = trlog(R)``` as above but returns directly `theta` the rotation
angle and `w` (3&times;1) the unit-vector indicating the rotation axis.


```S = trlog(T)``` is the matrix logarithm (4&times;4) of `T` (4&times;4) which has a
skew-symmetric upper-left 3&times;3 submatrix corresponding to the vector
`theta`*`w` where `theta` is the rotation angle and `w` (3&times;1) is a unit-vector
indicating the rotation axis, and a translation component.


```[theta,twist] = trlog(T)``` as above but returns directly `theta` the rotation
angle and a `twist` vector (6&times;1) comprising [v `w`].
### Notes
* Efficient closed-form solution of the matrix logarithm for arguments that are    SO(3) or SE(3).
* Special cases of rotation by odd multiples of pi are handled.
* Angle is always in the interval [0,pi].
* There is no Toolbox function for SO(2) or SE(2), use LOGM instead.

### References
* Robotics, Vision & Control: Second Edition, P. Corke, Springer 2016; p43.
* Mechanics, planning and control, Park & Lynch, Cambridge, 2016.

### See also

[trexp](trexp.md), [trexp2](trexp2.md), [Twist](Twist.md), [logm](logm.md)
