---
---
# tr2angvec
_Convert rotation matrix to angle-vector form_


```[THETA,V] = TR2ANGVEC(R, OPTIONS)``` is rotation expressed in terms of an
angle `THETA` (1&times;1) about the axis `V` (1&times;3) equivalent to the orthonormal rotation
matrix `R` (3&times;3).


```[THETA,V] = TR2ANGVEC(T, OPTIONS)``` as above but uses the rotational part of the
homogeneous transform `T` (4&times;4).


If `R` (3&times;3&times; K) or `T` (4&times;4&times; K) represent a sequence then `THETA` (K&times;1)is a vector
of angles for corresponding elements of the sequence and `V` (K&times;3) are the
corresponding axes, one per row.
### Options
| | |
|---|---|
| `'deg'` | Return angle in degrees (default radians) |


### Notes
* For an identity rotation matrix both `THETA` and `V` are set to zero.
* The rotation angle is always in the interval [0 pi], negative rotation    is handled by inverting the direction of the rotation axis.
* If no output arguments are specified the result is displayed.

### See also

[angvec2r](angvec2r.md), [angvec2tr](angvec2tr.md), [trlog](trlog.md)
