Ruby Debugger Guide
===================

This gives a definition of every command in the ruby debugger.

### backtrace (bt)
Print the entire stack frame. Each frame is numbered, the most recent
frame is 0. frame number can be referred to in the "frame" command;
"up" and "down" add or subtract respectively to frame numbers shown.
The position of the current frame is marked with -->.

### break
set breakpoint to some position, (optionally) if expr == true

### catch (cat)
#### cat
catch info
#### cat <exception-name> [on|off]
Intercept <exception-name> when there would otherwise be no handler.
With an "on" or "off", turn handling the exception on or off.
#### cat off
delete all catchpoints

### condition
Condition breakpoint-number expression
Specify breakpoint number N to break only if COND is true.
N is an integer and COND is an expression to be evaluated whenever
breakpoint N is reached. If the empty string is used, the condition is removed.

### continue (c)
#### c
run until program ends or hits a breakpoint.
#### c <line-num>
run until program reaches line <line-num>

### delete (d)
delete some or all breakpoints

### display (disp)
#### displ <expression-name>
add expression into display expression list
#### displ
display expression list

### down
move to lower frame

### edit
Edit specified file.
With no argument, edits file containing most recent line listed.
Editing targets can also be specified in this:
FILE:LINENUM, to edit at that line in that file

### enable
Enable some things.
This is used to cancel the effect of the "disable" command.
--
List of enable subcommands:
--
enable breakpoints -- Enable specified breakpoints
enable display -- Enable some expressions to be displayed when program stops

### eval (e)
#### e <expression>
evaluate expression and print its value

### exit (quit, q)
exit from debugger.

### finish (fin)
#### fin <frame-num>
Execute until selected stack frame returns.

If no frame number is given, we run until the currently selected frame
returns.  The currently selected frame starts out the most-recent
frame or 0 if no frame positioning (e.g "up", "down" or "frame") has
been performed. If a frame number is given we run until that frame
returns.
