---
---
# trnorm
_Normalize an SO(3) or SE(3) matrix_


```TRNORM(R)``` is guaranteed to be a proper orthogonal matrix rotation
matrix (3&times;3) which is "close" to the input matrix `R` (3&times;3). If `R`
= [N,O,A] the O and A vectors are made unit length and the normal vector
is formed from N = O x A, and then we ensure that O and A are orthogonal
by O = A x N.


```TRNORM(T)``` as above but the rotational submatrix of the homogeneous
transformation `T` (4&times;4) is normalised while the translational part is
unchanged.


If `R` (3&times;3&times; K) or `T` (4&times;4&times; K) representing a sequence then the normalisation
is performed on each of the K planes.
### Notes
* Only the direction of A (the z-axis) is unchanged.
* Used to prevent finite word length arithmetic causing transforms to    become `unnormalized'.
* There is no Toolbox function for SO(2) or SE(2).

### See also

[oa2tr](oa2tr.md), [SO3.trnorm](SO3.trnorm.md), [SE3.trnorm](SE3.trnorm.md)
