### Customizing Aptitudes package list

Escape | Name | Default size | Expandable | Description
-------|------|--------------|------------|------------
%% | Literal % | 1 | No | This is not really an escape; it simply inserts a percent sign into the output at the point at which it occurs.
%#number | Parameter Replacement | Variable | No | In some circumstances, a display format string will have “parameters”: for instance, in the command-line search, the groups matched by the search are used as parameters when displaying the result. This format code will be replaced by the parameter indicated by number.
%a | Action Flag | 1 | No | A single-character flag summarizing any action to be performed on the package, as described in Figure 2.10, “Values of the “action” flag”.
%A | Action | 10 | No | A somewhat more verbose description of the action to be performed on the package.
%B | Broken Count | 12 | No | If there are no broken packages, produces nothing. Otherwise, produces a string such as “Broken: 10” describing the number of broken packages.
%c | Current State Flag | 1 | No | A single-character flag summarizing the current state of the package, as described in Figure 2.9, “Values of the “current state” flag”.
%C | Current State | 11 | No | A more verbose description of the current state of the package.
%d | Description | 40 | Yes | The package's short description.
%D | Package Size | 8 | No | The size of the package file containing the package.
%H | Hostname | 15 | No | The name of the computer on which aptitude is running.
%i | Pin priority | 4 | No | Displays the highest priority assigned to a package version; for packages, displays the priority of the version which will be forced to be installed (if any).
%I | Installed Size | 8 | No | The (estimated) amount of space the package takes up on disk.
%m | Maintainer | 30 | Yes | The maintainer of the package.
%M | Automatic Flag | 1 | No | If the package is automatically installed, outputs “A”; otherwise, outputs nothing.
%n | Program Version | The length of “0.6.11”. | No | Outputs the version of aptitude that is running, currently “0.6.11”.
%N | Program Name | The length of the name. | No | Outputs the name of the program; usually “aptitude”.
%o | Download Size | 17 | No | If no packages are going to be installed, outputs nothing. Otherwise, outputs a string describing the total size of all the package files which will be installed (an estimate of how much needs to be downloaded); for instance, “DL size: 1000B”.
%p | Package Name | 30 | Yes | Outputs the name of the package. When a package is displayed in a tree context, the name of the package will be indented, if possible, according to its depth in the tree.
%P | Priority | 9 | No | Outputs the priority of the package.
%r | Reverse Depends Count | 2 | No | Outputs the approximate number of installed packages which depend upon the package.
%R | Abbreviated Priority | 3 | No | Outputs an abbreviated description of the package's priority: for instance, “Important” becomes “Imp”.
%s | Section | 10 | No | Outputs the section of the package.
%S | Trust Status | 1 | No | If the package is untrusted, displays the letter "U".
%t | Archive | 10 | Yes | The archive in which the package is found.
%T | Tagged | 1 | No | Outputs “*” if the package is tagged, nothing otherwise.[19]
%u | Disk Usage Change | 30 | No | If the scheduled actions will alter the amount of space used on the disk, outputs a description of the change in disk space; for instance, “Will use 100MB of disk space.”
%v | Current Version | 14 | No | Outputs the currently installed version of the package, or <none> if the package is not currently installed.
%V | Candidate Version | 14 | No | Outputs the version of the package which would be installed if Package ? Install (+) were issued on the package, or <none> if the package is not currently available.
%Z | Size Change | 9 | No | Outputs how much additional space will be used or how much space will be freed by installing, upgrading, or removing a package.

Source: https://aptitude.alioth.debian.org/doc/en/ch02s05s01.html