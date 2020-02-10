---
layout: default
parent: homogeneous functions
---
# tr2eul
_Convert SO(3) or SE(3) matrix to Euler angles_


```EUL = TR2EUL(T, OPTIONS)``` are the ZYZ Euler angles (1&times;3) corresponding to
the rotational part of a homogeneous transform `T` (4&times;4). The 3 angles
`EUL`=[PHI,THETA,PSI] correspond to sequential rotations about the Z, Y and
Z axes respectively.


```EUL = TR2EUL(R, OPTIONS)``` as above but the input is an orthonormal
rotation matrix `R` (3&times;3).


If `R` (3&times;3&times; K) or `T` (4&times;4&times; K) represent a sequence then each row of `EUL`
corresponds to a step of the sequence.
### Options

| | |
|---|---|
| `'deg'` | Compute angles in degrees (radians default) |
| `'flip'` | Choose first Euler angle to be in quadrant 2 or 3. |


### Notes
* There is a singularity for the case where THETA=0 in which case PHI is arbitrarily    set to zero and PSI is the sum (PHI+PSI).
* Translation component is ignored.

### See also

[eul2tr](eul2tr.md), [tr2rpy](tr2rpy.md)
