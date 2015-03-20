# pathtools (pt-*)
A set of tools for viewing, manipulating and managing path environmental variables

I chose to write the tools in bash since I feel it reduces the dependencies.

I decided to split things into several tools (a tool suite) rather than have one all-seeing, all-doing command line tool.
I think this makes usage easier - you can easily get each tools functionality into your head and there's no clutter with the options.

Each tool is named to allow you to guess it's function:

* Pretty Printing  -  (pt-print)
* Selecting/Greping entries  -  (pt-grep)
* Sorting entries  -  (pt-sort)
* Removing/Deleting entries  -  (pt-del)

The tools are designed to use STDIN if provided and $PATH as default (if no STDIN is given)
This makes things straight forward and the STDIN option also lets you chain the tools together via a simple pipe (this adds flexibility).

The tools are designd to be non-destructive (i.e. none of them modify the PATH you provide).
If you wish to modify the PATH you can assign the output of one of the pt-* tools to it.

e.g.)

export PATH=$(echo $PATH | ./pt-grep -r bin) 

This may not be too pretty but it works.


