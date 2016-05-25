# System X
System X is a set of clients and daemons to enable the fundamental operations of modern POSIX(-like) systems.  You could call it a replacement for Systemd with a different philosophy.

# Goals
The goals for System X are derived from the wisdom I've gained from experience as well as the wisdom of the [Unix philosophy](https://en.wikipedia.org/wiki/Unix_philosophy).

* Small footprint - The entire system should fit on a floppy.
* Portability - Only rely on [POSIX](https://en.wikipedia.org/wiki/POSIX), [C++](https://en.wikipedia.org/wiki/C%2B%2B_Standard_Library) and [FUSE](https://en.wikipedia.org/wiki/Filesystem_in_Userspace).
* Multi-platform support - At compile-time, use custom code to support specific kernels when most beneficial.
* Fault tolerance - Recover from errors or fail gracefully but don't hang or crash.
* Modularity, not tight integration - Components should be trivial to replace.
* Text, not binaries - Configuration and log files should be readable with a generic text editor.
* Well documented - Generated documentation and code comments are not sufficient.

# Components
System X components currently being worked on.
* [Public Domain Toolkit](https://github.com/GravisZro/pdtk) - A minimalist event-driven toolkit that can be compiled into any program.
* [Magic Circle File System](https://github.com/GravisZro/mcfs) - A FUSE filesystem to manage IPC sockets.
* [Incanto](https://github.com/GravisZro/incanto) - A code generator for using sockets in MCFS as an IPC mechanism.
* [System X Initializer](https://github.com/GravisZro/sxinit) - A minimal init system that ensure the system is ready for the System X Service Daemon.
* [System X Service Daemon](https://github.com/GravisZro/sxserviced) - A runlevel based service management daemon.
* [System X Configuration Daemon](https://github.com/GravisZro/sxconfigd) - Abstracts /etc configuration file interface/notifies of configuration updates.
* [System X System Logger Daemon](https://github.com/GravisZro/sxsyslogd) - A RFC compliant system logger that logs in an efficient searchable text format.
* [System X Logging Daemon](https://github.com/GravisZro/sxlogd) - A reliable file logger that refuses to fail.
* [System X Session Daemon](https://github.com/GravisZro/sxsessiond) - A generic session manager.
* More to come.
