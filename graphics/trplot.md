---
layout: default
parent: List of graphics functions
---
# trplot
_Plot a 3D coordinate frame_


```TRPLOT(T, OPTIONS)``` draws a 3D coordinate frame represented by the SE(3) homogeneous
transform `T` (4&times;4).


```H = TRPLOT(T, OPTIONS)``` as above but returns a handle.


```TRPLOT(R, OPTIONS)``` as above but the coordinate frame is rotated about the
origin according to the orthonormal rotation matrix `R` (3&times;3).


```H = TRPLOT(R, OPTIONS)``` as above but returns a handle.


```H = TRPLOT()``` creates a default frame EYE(3,3) at the origin and returns a
handle.
### Animation


Firstly, create a plot and keep the the handle as per above.


```TRPLOT(H, T)``` moves the coordinate frame described by the handle `H` to
the pose `T` (4&times;4).
### Options

| | |
|---|---|
| `'handle',h` | Update the specified handle |
| `'axhandle',A` | Draw in the MATLAB axes specified by the axis handle A |
| `` |  |
| `'color',C` | The color to draw the axes, MATLAB ColorSpec |
| `'axes'` | Show the MATLAB axes, box and ticks (default true) |
| `'axis',A` | Set dimensions of the MATLAB axes to A=[xmin xmax ymin ymax zmin zmax] |
| `'frame',F` | The coordinate frame is named {F} and the subscript on the axis labels is F. |
| `'framelabel',F` | The coordinate frame is named {F}, axes have no subscripts. |
| `'framelabeloffset',O` | Offset O=[DX DY] frame labels in units of text box height |
| `'text_opts', opt` | A cell array of MATLAB text properties |
| `'length',s` | Length of the coordinate frame arms (default 1) |
| `'thick',t` | Thickness of lines (default 0.5) |
| `'text'` | Enable display of X,Y,Z labels on the frame (default true) |
| `'labels',L` | Label the X,Y,Z axes with the 1st, 2nd, 3rd character of the string L |
| `'rgb'` | Display X,Y,Z axes in colors red, green, blue respectively |
| `'rviz'` | Display chunky rviz style axes% |
| `'arrow'` | Use arrows rather than line segments for the axes |
| `'width', w` | Width of arrow tips (default 1) |
| `` |  |
| `'perspective'` | Display the axes with perspective projection (default off) |
| `'3d'` | Plot in 3D using anaglyph graphics |
| `'anaglyph',A                         left and right (default colors 'rc'): chosen from` | Specify anaglyph colors for '3d' as 2 characters for |
| `` | r)ed, g)reen, b)lue, c)yan, m)agenta. |
| `'dispar',D` | Disparity for 3d display (default 0.1) |
| `'view',V                         for view toward origin of coordinate frame` | Set plot view parameters V=[az el] angles, or 'auto' |
| `'lefty'` | Draw left-handed frame (dangerous) |


### Examples


```trplot(T, 'frame', 'A')```
trplot(`T`, 'frame', 'A', 'color', 'b')
trplot(T1, 'frame', 'A', 'text_opts', {'FontSize', 10, 'FontWeight', 'bold'})
trplot(T1, 'labels', 'NOA');


```h = trplot(T, 'frame', 'A', 'color', 'b')```;
trplot(`h`, T2);


3D anaglyph plot


```trplot(T, '3d')```;
### Notes
* Multiple frames can be added using the HOLD command
* When animating a coordinate frame it is best to set the axis bounds initially.
* The 'rviz' option is equivalent to 'rgb', 'notext', 'noarrow',    'thick', 5.
* The 'arrow' option requires https://www.mathworks.com/matlabcentral/fileexchange/14056-arrow3

