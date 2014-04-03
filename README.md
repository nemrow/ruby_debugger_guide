Ruby Debugger Guide
===================

This gives a definition of every command in the ruby debugger.

== backtrace (bt)
Print the entire stack frame. Each frame is numbered, the most recent
frame is 0. frame number can be referred to in the "frame" command;
"up" and "down" add or subtract respectively to frame numbers shown.
The position of the current frame is marked with -->.

== break
set breakpoint to some position, (optionally) if expr == true
