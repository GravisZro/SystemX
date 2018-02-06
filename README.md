# ![System X](https://github.com/GravisZro/SystemX/blob/master/systemx.png)
System X is a modernized implementation of a POSIX system.  It can replace both UNIX System V and Linux's Systemd or be partly used to supplement an existing system.

# Goals
The goals for System X are derived from the wisdom I've gained from experience as well as the wisdom of the [Unix philosophy](https://en.wikipedia.org/wiki/Unix_philosophy).

* Small footprint - The entire system should fit on a floppy.
* Portability - Only rely on [POSIX](https://en.wikipedia.org/wiki/POSIX), [C++](https://en.wikipedia.org/wiki/C%2B%2B_Standard_Library) and statically linked platform libraries with the same restrictions.
* Multi-platform support - At compile-time, use custom code to support specific kernels when most beneficial.
* Fault tolerance - Recover from errors or fail gracefully but don't hang or crash.
* Modular but integrated - Components should be trivial to replace and able to work together or function independently.
* Text, not binaries - Configuration and log files should be readable with a generic text editor.
* Well documented - Generated documentation and code comments are not sufficient.

# Non-POSIX Defined Components
System X components currently being worked on.
## System Components
* [Service Connector File System](https://github.com/GravisZro/scfs) - A [FUSE](https://en.wikipedia.org/wiki/Filesystem_in_Userspace) filesystem to manage service sockets.  
* [Initializer](https://github.com/GravisZro/SXinit) - A minimal init system that ensures the SCFS is mounted, Config daemon runs then Director daemon runs or bails out to an emergency shell.
* [Executor](https://github.com/GravisZro/executor) - A small tool to setup an environment for and then execute a program.
* [Director Daemon](https://github.com/GravisZro/SXdirector) - A dependency and runlevel based daemon management daemon.
* [Configuration Daemon](https://github.com/GravisZro/SXconfig) - Abstracts /etc configuration file interface/notifies of configuration updates.
* [System Logger Daemon](https://github.com/GravisZro/SXsyslog) - A RFC compliant system logger that logs in an efficient searchable text format.
* [Logging Daemon](https://github.com/GravisZro/SXlog) - A reliable file logger that refuses to fail.
* [Event Daemon](https://github.com/GravisZro/SXevent) - A hardware event notification daemon.
* [Device Daemon](https://github.com/GravisZro/SXdev) - A devfs maintenance daemon.

## Development Components
* [Public Domain Toolkit](https://github.com/GravisZro/pdtk) - A minimalist event-driven toolkit that can be compiled into any program.
* [Incanto](https://github.com/GravisZro/incanto) - A code generator for using sockets in SCFS as an IPC mechanism.
