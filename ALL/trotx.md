---
layout: default
parent: ALL functions
---
# trotx
_SE(3) rotation about X axis_


```T = TROTX(THETA)``` is a homogeneous transformation (4&times;4) representing a rotation
of `THETA` radians about the x-axis.


```T = TROTX(THETA, 'deg')``` as above but `THETA` is in degrees.
### Notes
* Translational component is zero.

### See also

[rotx](rotx.md), [troty](troty.md), [trotz](trotz.md), [trot2](trot2.md), [SE3.Rx](SE3.Rx.md)
