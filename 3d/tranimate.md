---
layout: default
parent: 3d functions
---
# tranimate
_Animate a 3D coordinate frame_


```TRANIMATE(P1, P2, OPTIONS)``` animates a 3D coordinate frame moving from pose X1
to pose X2.  Poses X1 and X2 can be represented by:
* SE(3) homogeneous transformation matrices (4&times;4)
* SO(3) orthonormal rotation matrices (3&times;3)



```TRANIMATE(X, OPTIONS)``` animates a coordinate frame moving from the identity pose
to the pose `X` represented by any of the types listed above.


```TRANIMATE(XSEQ, OPTIONS)``` animates a trajectory, where `XSEQ` is any of
* SE(3) homogeneous transformation matrix sequence (4&times;4&times; N)
* SO(3) orthonormal rotation matrix sequence (3&times;3&times; N)

### Options

| | |
|---|---|
| `'fps', fps` | Number of frames per second to display (default 10) |
| `'nsteps', n` | The number of steps along the path (default 50) |
| `'axis',A` | Axis bounds [xmin, xmax, ymin, ymax, zmin, zmax] |
| `'movie',M` | Save frames as a movie or sequence of frames |
| `'cleanup'` | Remove the frame at end of animation |
| `'noxyz'` | Don't label the axes |
| `'rgb'` | Color the axes in the order x=red, y=green, z=blue |
| `'retain'` | Retain frames, don't animate |




Additional options are passed through to TRPLOT.
### Notes
* Uses the Animate helper class to record the frames.

### See also

[trplot](trplot.md), [Animate](Animate.md), [SE3.animate](SE3.animate.md)
