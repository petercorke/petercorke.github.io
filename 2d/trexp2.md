---
layout: default
parent: List of 2d functions
---
# trexp2
_Matrix exponential for so(2) and se(2)_
### SO(2)


```R = TREXP2(OMEGA)``` is the matrix exponential (2&times;2) of the so(2) element `OMEGA` that
yields a rotation matrix (2&times;2).


```R = TREXP2(THETA)``` as above, but rotation by `THETA` (1&times;1).
### SE(2)


```T = TREXP2(SIGMA)``` is the matrix exponential (3&times;3) of the se(2) element
`SIGMA` that yields a homogeneous transformation  matrix (3&times;3).


```T = TREXP2(SIGMA, THETA)``` as above, but se(2) rotation of `SIGMA`*`THETA`, the
rotation part of `SIGMA` (3&times;3) must be unit norm.


```T = TREXP2(TW)``` as above, but the se(2) value is expressed as a vector `TW`
(1&times;3).


```T = TREXP(TW, THETA)``` as above, but se(2) rotation of `TW`*`THETA`, the
rotation part of `TW` must be unit norm.
### Notes
* Efficient closed-form solution of the matrix exponential for arguments that are    so(2) or se(2).
* If `THETA` is given then the first argument must be a unit vector or a    skew-symmetric matrix from a unit vector.

### References
* Robotics, Vision & Control: Second Edition, P. Corke, Springer 2016; p25-26.
* Mechanics, planning and control, Park & Lynch, Cambridge, 2017.

### See also

[trexp](trexp.md), [skew](skew.md), [skewa](skewa.md), [Twist](Twist.md)
