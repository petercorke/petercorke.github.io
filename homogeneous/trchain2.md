---
layout: default
parent: homogeneous functions
---
# trchain2
_Compound SE(2) transforms from string_


```T = TRCHAIN(S)``` is a homogeneous transform (3&times;3) that results from
compounding a number of elementary transformations defined by the string
`S`.  The string `S` comprises a number of tokens of the form X(ARG) where
X is one of Tx, Ty, or R.  ARG is an arbitrary MATLAB expression
that can include constants or workspace variables. For example:
```matlab
    trchain('Tx(1) R(90) Ty(2)')```


is equivalent to computing
```matlab
  transl2(1,0) * trot2(90, 'deg') * transl2(0,2)```


```T = TRCHAIN(S, Q)``` as above but the expression for ARG can also contain
a variable 'qJ' which selects the Jth value from the passed vector `Q` (1&times;N).
For example:
```matlab
  trchain('Tx(1) R(q1-90) Ty(2) R(q2)', [1 2])```


[`T`,TOK] = TRCHAIN(`S` ...) as above but return an array of tokens which can
be passed in, instead of the string.


`T` = TRCHAIN(TOK ...) as above but chain is defined by array of tokens
instead of a string.
### Options

| | |
|---|---|
| `- 'deg'` | all angular variables are in degrees (default radians) |
| `- 'qvar',V` | treat the string V as the joint variable name rather than 'q' |


### Notes
* Variables used in the string must exist in the caller workspace.
* The string can contain arbitrary characters between the elements, for    example space, +, *, . or even &vert;.
* Works for symbolic variables in the workspace and/or passed in via the    vector `Q`.
* For symbolic operations that involve use of the value pi, make sure you    define it first in the workspace: pi = sym('pi');
* The tokens are simply a parsed version of the input string and provide    some efficiency for repeated calls on the same chain.

### See also

[trchain2](trchain2.md), [trotx](trotx.md), [troty](troty.md), [trotz](trotz.md), [transl](transl.md), [SerialLink.trchain](SerialLink.trchain.md), [ets](ets.md)
