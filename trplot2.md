---
---
# trplot2
_Plot a 2D coordinate frame_


```TRPLOT2(T, OPTIONS)``` draws a 2D coordinate frame represented by the SE(2)
homogeneous transform `T` (3&times;3).


```H = TRPLOT2(T, OPTIONS)``` as above but returns a handle.


```TRPLOT(R, OPTIONS)``` as above but the coordinate frame is rotated about the
origin according to the orthonormal rotation matrix `R` (2&times;2).


```H = TRPLOT(R, OPTIONS)``` as above but returns a handle.


```H = TRPLOT2()``` creates a default frame EYE(2,2) at the origin and returns a
handle.
### Animation


Firstly, create a plot and keep the the handle as per above.


```TRPLOT2(H, T)``` moves the coordinate frame described by the handle `H` to
the SE(2) pose `T` (3&times;3).
### Options
| | |
|---|---|
| `'handle',h` | Update the specified handle |
| `'axhandle',A` | Draw in the MATLAB axes specified by the axis handle A |
| `` |  |
| `'color', c` | The color to draw the axes, MATLAB ColorSpec |
| `'axes'` | Show the MATLAB axes, box and ticks (default true) |
| `'axis',A` | Set dimensions of the MATLAB axes to A=[xmin xmax ymin ymax] |
| `'frame',F` | The frame is named {F} and the subscript on the axis labels is F. |
| `'framelabel',F` | The coordinate frame is named {F}, axes have no subscripts. |
| `'framelabeloffset',O` | Offset O=[DX DY] frame labels in units of text box height |
| `'text_opts', opt` | A cell array of Matlab text properties |
| `'length',s` | Length of the coordinate frame arms (default 1) |
| `'thick',t` | Thickness of lines (default 0.5) |
| `'text'` | Enable display of X,Y,Z labels on the frame (default true) |
| `'labels',L` | Label the X,Y,Z axes with the 1st and 2nd character of the string L |
| `'arrow'` | Use arrows rather than line segments for the axes |
| `'width', w` | Width of arrow tips |
| `'lefty'` | Draw left-handed frame (dangerous) |


### Examples


```trplot2(T, 'frame', 'A')```
trplot2(`T`, 'frame', 'A', 'color', 'b')
trplot2(T1, 'frame', 'A', 'text_opts', {'FontSize', 10, 'FontWeight', 'bold'})
### Notes
* Multiple frames can be added using the HOLD command
* When animating a coordinate frame it is best to set the axis bounds initially.
* The 'arrow' option requires https://www.mathworks.com/matlabcentral/fileexchange/14056-arrow3

### See also

[trplot](trplot.md)
