---
---
# tb_optparse
_Standard option parser for Toolbox functions_


```OPTOUT = TB_OPTPARSE(OPT, ARGLIST)``` is a generalized option parser for
Toolbox functions.  `OPT` is a structure that contains the names and
default values for the options, and `ARGLIST` is a cell array containing
option parameters, typically it comes from VARARGIN.  It supports options
that have an assigned value, boolean or enumeration types (string or
int).


```[OPTOUT,ARGS] = TB_OPTPARSE(OPT, ARGLIST)``` as above but returns all the
unassigned options, those that don't match anything in `OPT`, as a cell
array of all unassigned arguments in the order given in `ARGLIST`.


```[OPTOUT,ARGS,LS] = TB_OPTPARSE(OPT, ARGLIST)``` as above but if any
unmatched option looks like a MATLAB LineSpec (eg. 'r:') it is placed in `LS` rather
than in `ARGS`.


```[OBJOUT,ARGS,LS] = TB_OPTPARSE(OPT, ARGLIST, OBJ)``` as above but properties
of `OBJ` with matching names in `OPT` are set.


The software pattern is:
```matlab
   function myFunction(a, b, c, varargin)
      opt.foo = false;
      opt.bar = true;
      opt.blah = [];
      opt.stuff = {};
      opt.choose = {'this', 'that', 'other'};
      opt.select = {'#no', '#yes'};
      opt.old = '@foo';
      opt = tb_optparse(opt, varargin);

```


Optional arguments to the function behave as follows:
| | |
|---|---|
| `'foo'` | sets opt.foo := true |
| `'nobar'` | sets opt.foo := false |
| `'blah', 3` | sets opt.blah := 3 |
| `'blah',{x,y}` | sets opt.blah := {x,y} |
| `'that'` | sets opt.choose := 'that' |
| `'yes'` | sets opt.select := 2 (the second element) |
| `'stuff', 5` | sets opt.stuff to {5} |
| `'stuff', {'k',3}` | sets opt.stuff to {'k',3} |
| `'old'` | synonym, is the same as the option foo |




and can be given in any combination.


If neither of 'this', 'that' or 'other' are specified then opt.choose := 'this'.
Alternatively if:
```matlab
  opt.choose = {[], 'this', 'that', 'other'};
```


then if neither of 'this', 'that' or 'other' are specified then opt.choose := [].


If neither of 'no' or 'yes' are specified then opt.select := 1.


The return structure is automatically populated with fields: verbose and
debug.  The following options are automatically parsed:
| | |
|---|---|
| `'verbose'` | sets opt.verbose := true |
| `'verbose=2'` | sets opt.verbose := 2 (very verbose) |
| `'verbose=3'` | sets opt.verbose := 3 (extremeley verbose) |
| `'verbose=4'` | sets opt.verbose := 4 (ridiculously verbose) |
| `'debug', N` | sets opt.debug := N |
| `'showopt'` | displays opt and arglist |
| `'setopt',S                    opt.foo is set to 4.` | sets opt := S, if S.foo=4, and opt.foo is present, then |




The allowable options are specified by the names of the fields in the
structure `OPT`.  By default if an option is given that is not a field of
`OPT` an error is declared.
### Notes
* That the enumerator names must be distinct from the field names.
* That only one value can be assigned to a field, if multiple values    are required they must placed in a cell array.
* If the option is seen multiple times the last (rightmost) instance applies.
* To match an option that starts with a digit, prefix it with 'd_', so    the field 'd_3d' matches the option '3d'.
* Any input argument or element of the opt struct can be a string instead    of a char array.

