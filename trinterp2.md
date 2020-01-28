---
---
# trinterp2
_Interpolate SE(2) homogeneous transformations_


```TRINTERP2(T0, T1, S)``` is a homogeneous transform (3&times;3) interpolated
between `T0` when `S`=0 and `T1` when `S`=1.  `T0` and `T1` are both homogeneous
transforms (4&times;4).  If `S` (N&times;1) then T (3&times;3&times; N) is a sequence of
homogeneous transforms corresponding to the interpolation values in `S`.


```TRINTERP2(T1, S)``` as above but interpolated between the identity matrix
when `S`=0 to `T1` when `S`=1.


```TRINTERP2(T0, T1, M)``` as above but `M` is a positive integer and return a
sequence (4&times;4&times; `M`) of homogeneous transforms linearly interpolating between
`T0` and `T1` in `M` steps.


```TRINTERP2(T1, M)``` as above but return a sequence (4&times;4&times; `M`) of
homogeneous interpolating between identity matrix and `T1` in `M` steps.
### Notes
* `T0` or `T1` can also be an SO(2) rotation matrix (2&times;2).
* Rotation angle is linearly interpolated.
* To obtain smooth continuous motion `S` should also be smooth and continuous,    such as computed by tpoly or lspb.

### See also

[trinterp](trinterp.md), [SE3.interp](SE3.interp.md), [UnitQuaternion](UnitQuaternion.md), [tpoly](tpoly.md), [lspb](lspb.md)
