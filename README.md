# System X
System X is a set of clients and daemons to enable fundamental operation of modern POSIX systems.  You could call it a replacement for Systemd but with a different philosophy.

# Goals
* Small footprint - The entire system should fit on a floppy.
* Portability - Only rely on POSIX, C++14 and FUSE.
* Multi-platform support - At compile-time, use custom code to support specific kernels when most benificial.
* Fault tolerance - Recover from errors or fail gracefully but don't hang or crash.
* Modularity, not tight integration - Components should be trivial to replace.
* Text, not binaries - Configuration and log files should be readable with a generic text editor.
* Well documented - Generated documentation and code comments are not sufficient.

# Components
* circlefs
