---
layout: default
parent: TOC_differential
---
# trexp
_Matrix exponential for so(3) and se(3)_
### For so(3)


```R = TREXP(OMEGA)``` is the matrix exponential (3&times;3) of the so(3) element `OMEGA` that
yields a rotation matrix (3&times;3).


```R = TREXP(OMEGA, THETA)``` as above, but so(3) motion of `THETA`*`OMEGA`.


```R = TREXP(S, THETA)``` as above, but rotation of `THETA` about the unit vector `S`.


```R = TREXP(W)``` as above, but the so(3) value is expressed as a vector `W`
(1&times;3) where `W` = `S` * `THETA`. Rotation by &vert;&vert;`W`&vert;&vert; about the vector `W`.
### For se(3)


```T = TREXP(SIGMA)``` is the matrix exponential (4&times;4) of the se(3) element `SIGMA` that
yields a homogeneous transformation  matrix (4&times;4).


```T = TREXP(SIGMA, THETA)``` as above, but se(3) motion of `SIGMA`*`THETA`, the
rotation part of `SIGMA` (4&times;4) must be unit norm.


```T = TREXP(TW)``` as above, but the se(3) value is expressed as a twist vector `TW`
(1&times;6).


```T = TREXP(TW, THETA)``` as above, but se(3) motion of `TW`*`THETA`, the
rotation part of `TW` (1&times;6) must be unit norm.
### Notes
* Efficient closed-form solution of the matrix exponential for arguments that are    so(3) or se(3).
* If `THETA` is given then the first argument must be a unit vector or a    skew-symmetric matrix from a unit vector.
* Angle vector argument order is different to ANGVEC2R.

### References
* Robotics, Vision & Control: Second Edition, P. Corke, Springer 2016; p42-43.
* Mechanics, planning and control, Park & Lynch, Cambridge, 2017.

### See also

[angvec2r](angvec2r.md), [trlog](trlog.md), [trexp2](trexp2.md), [skew](skew.md), [skewa](skewa.md), [Twist](Twist.md)
