These are the source codes for a small initializer package required to store FreeBSD files and directories on the PS3's HDD.
Add a USRDIR and add the `bin`, `etc`, `lib`, `libexec`, `media`, `root`, `sbin`, `usr`, and `var` directories to it. (These are required.)
Also, don't forget to place empty files in all of these directories. If you forget these workarounds, the PS3 will not create directories, and BSD will not work!
