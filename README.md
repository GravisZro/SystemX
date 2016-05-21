# System X
System X is a set of clients and daemons to enable the fundamental operations of modern POSIX(-like) systems.  You could call it a replacement for Systemd with a different philosophy.

# Goals
The goals for System X are derived from the wisdom I've gained from experience as well as the wisdom of the [Unix philosophy](https://en.wikipedia.org/wiki/Unix_philosophy).

* Small footprint - The entire system should fit on a floppy.
* Portability - Only rely on [POSIX](https://en.wikipedia.org/wiki/POSIX), [C++](https://en.wikipedia.org/wiki/C%2B%2B_Standard_Library) and [FUSE](https://en.wikipedia.org/wiki/Filesystem_in_Userspace).
* Multi-platform support - At compile-time, use custom code to support specific kernels when most benificial.
* Fault tolerance - Recover from errors or fail gracefully but don't hang or crash.
* Modularity, not tight integration - Components should be trivial to replace.
* Text, not binaries - Configuration and log files should be readable with a generic text editor.
* Well documented - Generated documentation and code comments are not sufficient.

# Components
System X components currently being worked on.
* [PDTK](https://github.com/GravisZro/pdtk) - A minimalist event-driven toolkit that can be compiled into any program.
* [circlefs](https://github.com/GravisZro/circlefs) - A FUSE filsystem to manage IPC sockets.
* incanto - A code generator for using sockets in circlefs as IPC mechanism.
* sysxinit - A minimal init/shutdown system that ensure the system is ready for sysxsmd.
* sysxsmd - A runlevel aware service management daemon.
* sysxconfd - Abstracts /etc configuration file interface/notifies of configuration updates.
* sysxlogd - A text file based system logger that enables better log searching.
* More to come.
