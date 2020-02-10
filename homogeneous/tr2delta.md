---
layout: default
parent: homogeneous functions
---
# tr2delta
_Convert SE(3) homogeneous transform to differential motion_


```D = TR2DELTA(T0, T1)``` is the differential motion (6&times;1) corresponding to
infinitessimal motion (in the `T0` frame) from pose `T0` to `T1` which are homogeneous
transformations (4&times;4) or SE3 objects.


The vector `D`=(dx, dy, dz, dRx, dRy, dRz) represents infinitessimal translation
and rotation, and is an approximation to the instantaneous spatial velocity
multiplied by time step.


```D = TR2DELTA(T)``` as above but the motion is from the world frame to the SE3
pose `T`.
### Notes
* `D` is only an approximation to the motion `T`, and assumes    that `T0` ~ `T1` or `T` ~ eye(4,4).
* Can be considered as an approximation to the effect of spatial velocity over a    a time interval, average spatial velocity multiplied by time.

### Reference
* Robotics, Vision & Control: Second Edition, P. Corke, Springer 2016; p67.

### See also

[delta2tr](delta2tr.md), [skew](skew.md), [SE3.todelta](SE3.todelta.md)
