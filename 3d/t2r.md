---
layout: default
parent: List of 3d functions
---
# t2r
_Rotational submatrix_


```R = T2R(T)``` is the orthonormal rotation matrix component of homogeneous
transformation matrix `T`.  Works for `T` in SE(2) or SE(3)
* If `T` is 4&times;4, then `R` is 3&times;3.
* If `T` is 3&times;3, then `R` is 2&times;2.

### Notes
* For a homogeneous transform sequence (K&times;K&times; N) returns a rotation matrix    sequence (K-1&times;K-1&times;N).
* The validity of rotational part is not checked

### See also

[r2t](r2t.md), [tr2rt](tr2rt.md), [rt2tr](rt2tr.md)
