---
layout: default
parent: homogeneous functions
---
# trotz
_SE(3) rotation about Z axis_


```T = trotz(THETA)``` is a homogeneous transformation (4&times;4) representing a rotation
of `THETA` radians about the z-axis.


```T = trotz(THETA, 'deg')``` as above but `THETA` is in degrees.
### Notes
* Translational component is zero.

### See also

[rotz](rotz.md), [trotx](trotx.md), [troty](troty.md), [trot2](trot2.md), [SE3.Rz](SE3.Rz.md)
