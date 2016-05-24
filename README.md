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
* [PDTK](https://github.com/GravisZro/pdtk) - Public Domain Toolkit - A minimalist event-driven toolkit that can be compiled into any program.
* [mcfs](https://github.com/GravisZro/mcfs) - Magic Circle File System - A FUSE filesystem to manage IPC sockets.
* [incanto](https://github.com/GravisZro/incanto) - Incanto - A code generator for using sockets in MCFS as IPC mechanism.
* [sxinit](https://github.com/GravisZro/sxinit) - System X Initializer - A minimal init/shutdown system that ensure the system is ready for sxserviced.
* [sxserviced](https://github.com/GravisZro/sxserviced) - System X Service Daemon - A runlevel aware service management daemon.
* [sxconfigd](https://github.com/GravisZro/sxconfigd) - System X Configuration Daemon - Abstracts /etc configuration file interface/notifies of configuration updates.
* [sxlogd](https://github.com/GravisZro/sxlogd) - System X System Logger Daemon - A RFC compliant system logger that logs in an efficient searchable text format
* [sxlogd](https://github.com/GravisZro/sxlogd) - System X Logging Daemon - A reliable file logger that refuses to fail.
* [sxsessiond](https://github.com/GravisZro/sxsessiond) - System X Session Daemon - A generic session manager.
* More to come.
