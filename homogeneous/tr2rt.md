---
layout: default
parent: homogeneous functions
---
# tr2rt
_Convert homogeneous transform to rotation and translation_


```[R,t] = TR2RT(TR)``` splits a homogeneous transformation matrix (N&times;N) into an
orthonormal rotation matrix `R` (M&times;M) and a translation vector `t` (M&times;1), where
N=M+1.


Works for `TR` in SE(2) or SE(3)
* If `TR` is 4&times;4, then `R` is 3&times;3 and T is 3&times;1.
* If `TR` is 3&times;3, then `R` is 2&times;2 and T is 2&times;1.



A homogeneous transform sequence `TR` (N&times;N&times; K) is split into rotation matrix
sequence `R` (M&times;M&times; K) and a translation sequence `t` (K&times;M).
### Notes
* The validity of `R` is not checked.

### See also

[rt2tr](rt2tr.md), [r2t](r2t.md), [t2r](t2r.md)
