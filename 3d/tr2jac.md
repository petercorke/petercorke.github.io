---
layout: default
parent: 3d functions
---
# tr2jac
_Jacobian for differential motion_


```J = TR2JAC(TAB)``` is a Jacobian matrix (6&times;6) that maps spatial velocity or
differential motion from frame {A} to frame {B} where the pose of {B}
relative to {A} is represented by the homogeneous transform `TAB` (4&times;4).


```J = TR2JAC(TAB, 'samebody')``` is a Jacobian matrix (6&times;6) that maps spatial
velocity or differential motion from frame {A} to frame {B} where both
are attached to the same moving body.  The pose of {B} relative to {A} is
represented by the homogeneous transform `TAB` (4&times;4).
### See also

[wtrans](wtrans.md), [tr2delta](tr2delta.md), [delta2tr](delta2tr.md), [SE3.velxform](SE3.velxform.md)
