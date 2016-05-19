# System X
System X is a set of clients and daemons to enable the fundamental operations of modern POSIX(-like) systems.  You could call it a replacement for Systemd with a different philosophy.

# Goals
The goals for System X are derived from the wisdom I've gained from experience as well as the wisdom of the [Unix philosophy](https://en.wikipedia.org/wiki/Unix_philosophy).

* Small footprint - The entire system should fit on a floppy.
* Portability - Only rely on POSIX, C++14 and FUSE.
* Multi-platform support - At compile-time, use custom code to support specific kernels when most benificial.
* Fault tolerance - Recover from errors or fail gracefully but don't hang or crash.
* Modularity, not tight integration - Components should be trivial to replace.
* Text, not binaries - Configuration and log files should be readable with a generic text editor.
* Well documented - Generated documentation and code comments are not sufficient.

# Components

* [PDTK](https://github.com/GravisZro/pdtk) - A minimalist event-driven toolkit that can be compiled into any program.
* [circlefs](https://github.com/GravisZro/circlefs) - A FUSE filsystem to manage IPC sockets.
* incanto - An code generator for using sockets in circlefs as IPC mechanism.
* sysxinit - A minimal init/shutdown system that ensure the system is ready for sysxsmd.
* sysxsmd - A service management daemon that also manages run-levels and disk mounting.
* sysxconfd - Abstracts /etc configuration file interface/notifies of configuration updates.
* sysxlogd - A text file based system logger that enables better log searching.
