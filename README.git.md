# NCSA HTTPd Git repository

This repository is a fork of ["TooDumbForAName"'s ncsa-httpd repository](https://github.com/TooDumbForAName/ncsa-httpd) which assembled the known history of NCSA HTTPd's releases into a chronological development history.
We further extend this by making the last release (1.5.2a) buildable and usable on modern Linux and macOS systems.

Note that the minimum required is done to make the codebase buildable and usable.
This is intentional; there are many warnings during compilation and many bugs which are intentionally not fixed (we don't want to make an overly "patchy" fork of the original NCSA HTTPd).

To be clear, **DO NOT** use this in any sort of production or trusted environment.
It is literally over 20 years old and has many known exploits.

Please note that, unlike modern SCM practices, this repository rebases the primary branch.
For example, if an error was found with a commit, that commit is modified rather than being amended by a new commit later in the history.
As a result, `git pull` will not work.
Instead, to update:

```
$ git fetch origin
$ git reset --hard origin/main
```

## Legal
Portions developed at the National Center for Supercomputing Applications at the University of Illinois at Urbana-Champaign.

This is a modified derivative of NCSA HTTPd, and is **not** the original software.
Per the requirements of `COPYRIGHT`, the National Center for Supercomputing Applications has been notified of the distribution of this derivative work on 2020-07-29, and was acknowledged on 2020-10-20.
