---
parent: List of 3d functions
layout: default
---
# trscale
_Homogeneous transformation for pure scale_


```T = TRSCALE(S)``` is a homogeneous transform (4&times;4) corresponding to a pure
scale change.  If `S` is a scalar the same scale factor is used for x,y,z,
else it can be a 3-vector specifying scale in the x-, y- and
z-directions.
### Note
* This matrix does not belong to SE(3) and if compounded with    any SE(3) matrix the result will not be in SE(3).

