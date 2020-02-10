---
layout: default
parent: translation functions
---
# transl2
_SE(2) translational homogeneous transform_
### Create a translational SE(2) matrix


```T = TRANSL2(X, Y)``` is an SE(2) homogeneous transform (3&times;3) representing a
pure translation.


```T = TRANSL2(P)``` is a homogeneous transform representing a translation or
point `P`=[`X`,`Y`]. `P` (M&times;2) represents a sequence and `T` (3&times;3&times; M) is a
sequence of homogenous transforms such that `T`(:,:,i) corresponds to the
i'th row of `P`.
### Extract the translational part of an SE(2) matrix


```P = TRANSL2(T)``` is the translational part of a homogeneous transform as a
2-element column vector.  `T` (3&times;3&times; M) is a homogeneous transform
sequence and the rows of `P` (M&times;2) are the translational component of the
corresponding transform in the sequence.
### Notes
* Somewhat unusually, this function performs a function and its inverse.  An    historical anomaly.

### See also

[SE2.t](SE2.t.md), [rot2](rot2.md), [ishomog2](ishomog2.md), [trplot2](trplot2.md), [transl](transl.md)
