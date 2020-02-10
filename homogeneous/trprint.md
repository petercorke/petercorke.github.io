---
layout: default
parent: homogeneous functions
---
# trprint
_Compact display of SE(3) homogeneous transformation_


```TRPRINT(T, OPTIONS)``` displays the homogoneous transform (4&times;4) in a compact
single-line format.  If `T` is a homogeneous transform sequence then each
element is printed on a separate line.


```TRPRINT(R, OPTIONS)``` as above but displays the SO(3) rotation matrix (3&times;3).


```S = TRPRINT(T, OPTIONS)``` as above but returns the string.


TRPRINT `T` `OPTIONS` is the command line form of above.
