---
---
# transl
_SE(3) translational homogeneous transform_
### Create a translational SE(3) matrix


```T = TRANSL(X, Y, Z)``` is an SE(3) homogeneous transform (4&times;4) representing
a pure translation of `X`, `Y` and `Z`.


```T = TRANSL(P)``` is an SE(3) homogeneous transform (4&times;4) representing a
translation of `P`=[`X`,`Y`,`Z`]. `P` (M&times;3) represents a sequence and `T`
(4&times;4&times; M) is a sequence of homogeneous transforms such that `T`(:,:,i)
corresponds to the i'th row of `P`.
### Extract the translational part of an SE(3) matrix


```P = TRANSL(T)``` is the translational part of a homogeneous transform `T` as a
3-element column vector.  `T` (4&times;4&times; M) is a homogeneous transform
sequence and the rows of `P` (M&times;3) are the translational component of the
corresponding transform in the sequence.


```[X,Y,Z] = TRANSL(T)``` is the translational part of a homogeneous transform
`T` as three components.  If `T` (4&times;4&times; M) is a homogeneous transform sequence
then `X`,`Y`,`Z` (1&times;M) are the translational components of the corresponding
transform in the sequence.
### Notes
* Somewhat unusually, this function performs a function and its inverse.  An    historical anomaly.

### See also

[SE3.t](SE3.t.md), [SE3.transl](SE3.transl.md)
