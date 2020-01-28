---
---
# trprint2
_Compact display of SE(2) homogeneous transformation_


```TRPRINT2(T, OPTIONS)``` displays the homogoneous transform (3&times;3) in a compact
single-line format.  If `T` is a homogeneous transform sequence then each
element is printed on a separate line.


```TRPRINT2(R, OPTIONS)``` as above but displays the SO(2) rotation matrix (3&times;3).


```S = TRPRINT2(T, OPTIONS)``` as above but returns the string.


TRPRINT2 `T`  is the command line form of above, and displays in RPY format.
### Options
| | |
|---|---|
| `'radian'` | display angle in radians (default is degrees) |
| `'fmt', f` | use format string f for all numbers, (default %g) |
| `'label',l` | display the text before the transform |


### Examples
```matlab
  >> trprint2(T2)
  t = (0,0), theta = -122.704 deg

```
### See also

[trprint](trprint.md)
