# Python Standard Library (v. 3.11) - os - List of methods

Note: Most is copy pasted from the standard library documentation.

## Reference

https://docs.python.org/3/library/os.html

## Introduction

This module provides a portable way of using **operating system dependent functionality**. If you just want to **read or write a file see open()**, if you want to **manipulate paths, see the os.path module**, and if you want **to read all the lines in all the files on the command line see the fileinput module**. For creating **temporary files and directories see the tempfile module**, and for **high-level file and directory handling see the shutil module.**

## Process Parameters

- **os.ctermid**: Return the filename corresponding to the controlling terminal of the process.
- **os.environ**: A mapping object where keys and values are strings that represent the process environment. For example, environ['HOME'] is the pathname of your home directory (on some platforms), and is equivalent to getenv("HOME") in C.
- **os.environb**: Bytes version of environ: a mapping object where both keys and values are bytes objects representing the process environment. 
- **os.chdir, os.fchdir, os.getcwd**: These functions are described in Files and Directories.
- **os.fsencode**: Encode path-like filename to the filesystem encoding and error handler; return bytes unchanged.
- **os.fsdecode**: Decode the path-like filename from the filesystem encoding and error handler; return str unchanged.
- **os.fspath**: Return the file system representation of the path.
- **os.getenv**: Return the value of the environment variable key as a string if it exists, or default if it doesn’t. 
- **os.getenvb**: Return the value of the environment variable key as bytes if it exists, or default if it doesn’t.
- **os.get_exec_path**: Returns the list of directories that will be searched for a named executable, similar to a shell, when launching a process. 
- **os.getegid**: Return the effective group id of the current process. This corresponds to the “set id” bit on the file being executed in the current process.
- **os.geteuid**: Return the current process’s effective user id.
- **os.getgid**: Return the real group id of the current process.
- **os.getgrouplist**: Return list of group ids that user belongs to. 
- **os.getgroups**: Return list of supplemental group ids associated with the current process.
- **os.getlogin**: Return the name of the user logged in on the controlling terminal of the process. 
- **os.getpgid**: Return the process group id of the process with process id pid. If pid is 0, the process group id of the current process is returned.
- **os.getpgrp**: Return the id of the current process group.
- **os.getpid**: Return the current process id.
- **os.getppid**: Return the parent’s process id. 
- **os.getpriority**: Get program scheduling priority. The value which is one of PRIO_PROCESS, PRIO_PGRP, or PRIO_USER, and who is interpreted relative to which 
- **os.getresuid**: Return a tuple (ruid, euid, suid) denoting the current process’s real, effective, and saved user ids.
- **os.getresgid**: Return a tuple (rgid, egid, sgid) denoting the current process’s real, effective, and saved group ids.
- **os.getuid**: Return the current process’s real user id.
- **os.initgroups**: Call the system initgroups() to initialize the group access list with all of the groups of which the specified username is a member, plus the specified group id.
- **os.putenv**: Set the environment variable named key to the string value. Such changes to the environment affect subprocesses started with os.system(), popen() or fork() and execv().
- **os.setegid**: Set the current process’s effective group id.
- **os.seteuid**: Set the current process’s effective user id.
- **os.setgid**: Set the current process’ group id.
- **os.setgroups**: Set the list of supplemental group ids associated with the current process to groups. 
- **os.setpgrp**: Call the system call setpgrp() or setpgrp(0, 0) depending on which version is implemented (if any). See the Unix manual for the semantics.
- **os.setpgid**: Call the system call setpgid() to set the process group id of the process with id pid to the process group with id pgrp. 
- **os.setpriority**: Set program scheduling priority. 
- **os.setregid**: Set the current process’s real and effective group ids.
- **os.setresgid**: Set the current process’s real, effective, and saved group ids.
- **os.setresuid**: Set the current process’s real, effective, and saved user ids.
- **os.setreuid**: Set the current process’s real and effective user ids.
- **os.getsid**: Call the system call getsid(). See the Unix manual for the semantics.
- **os.setsid**: Call the system call setsid(). See the Unix manual for the semantics.
- **os.setuid**: Set the current process’s user id.
- **os.strerror:** Return the error message corresponding to the error code in code. On platforms where strerror() returns NULL when given an unknown error number, ValueError is raised.
- **os.supports_bytes_environ**: True if the native OS type of the environment is bytes (eg. False on Windows).
- **os.umask**: Set the current numeric umask and return the previous umask.
- **os.uname**: Returns information identifying the current operating system. The return value is an object with five attributes:
  - sysname - operating system name
  - nodename - name of machine on network (implementation-defined)
  - release - operating system release
  - version - operating system version
  - machine - hardware identifier
- **os.unsetenv**: Unset (delete) the environment variable named key. Such changes to the environment affect subprocesses started with os.system(), popen() or fork() and execv().

## File Operations

- **os.fdopen**: Return an open file object connected to the file descriptor fd. This is an alias of the open() built-in function and accepts the same arguments. 
- **os.close**: Close file descriptor fd.
- **os.closerange**: Close all file descriptors from fd_low (inclusive) to fd_high (exclusive), ignoring errors. Equivalent to (but much faster than):
- **os.copy_file_range**! Copy count bytes from file descriptor src, starting from offset offset_src, to file descriptor dst, starting from offset offset_dst. 
- **os.device_encoding** : Return a string describing the encoding of the device associated with fd if it is connected to a terminal; else return None.
- **os.dup**: Return a duplicate of file descriptor fd.
- **os.dup2**: Duplicate file descriptor fd to fd2, closing the latter first if necessary. Return fd2. 
- **os.fchmod**: Change the mode of the file given by fd to the numeric mode. See the docs for chmod() for possible values of mode. As of Python 3.3, this is equivalent to os.chmod(fd, mode).
- **os.fchown**: Change the owner and group id of the file given by fd to the numeric uid and gid. To leave one of the ids unchanged, set it to -1. See chown(). As of Python 3.3, this is equivalent to os.chown(fd, uid, gid).
- **os.fdatasync**: Force write of file with filedescriptor fd to disk. Does not force update of metadata.
- **os.fpathconf**: Return system configuration information relevant to an open file. 
- **os.fstat**: Get the status of the file descriptor fd. Return a stat_result object.
- **os.fstatvfs**: Return information about the filesystem containing the file associated with file descriptor fd, like statvfs().
- **os.fsync**: Force write of file with filedescriptor fd to disk. On Unix, this calls the native fsync() function; on Windows, the MS _commit() function.
- **os.ftruncate**: Truncate the file corresponding to file descriptor fd, so that it is at most length bytes in size. As of Python 3.3, this is equivalent to os.truncate(fd, length).
- **os.get_blocking**: Get the blocking mode of the file descriptor: False if the O_NONBLOCK flag is set, True if the flag is cleared.
- **os.isatty**: Return True if the file descriptor fd is open and connected to a tty(-like) device, else False.
- **os.lockf**: Apply, test or remove a POSIX lock on an open file descriptor. fd is an open file descriptor. cmd specifies the command to use - one of F_LOCK, F_TLOCK, F_ULOCK or F_TEST. len specifies the section of the file to lock.
- **os.login_tty**: Prepare the tty of which fd is a file descriptor for a new login session. 
- **os.lseek**: Set the current position of file descriptor fd to position pos, modified by how
- **os.open**: Open the file path and set various flags according to flags and possibly its mode according to mode. 
- **os.openpty**: Open a new pseudo-terminal pair. Return a pair of file descriptors (master, slave) for the pty and the tty, respectively. 
- **os.pipe**: Create a pipe. Return a pair of file descriptors (r, w) usable for reading and writing, respectively. The new file descriptor is non-inheritable.
- **os.pipe2**: Create a pipe with flags set atomically. flags can be constructed by ORing together one or more of these values: O_NONBLOCK, O_CLOEXEC.
- **os.posix_fallocate**: Ensures that enough disk space is allocated for the file specified by fd starting from offset and continuing for len bytes.
- **os.posix_fadvise**: Announces an intention to access data in a specific pattern thus allowing the kernel to make optimizations. 
- **os.pread**: Read at most n bytes from file descriptor fd at a position of offset, leaving the file offset unchanged.
- **os.preadv**: Read from a file descriptor fd at a position of offset into mutable bytes-like objects buffers, leaving the file offset unchanged.
- **os.pwrite**: Write the bytestring in str to file descriptor fd at position of offset, leaving the file offset unchanged.
- **os.pwritev**: Write the buffers contents to file descriptor fd at a offset offset, leaving the file offset unchanged. buffers must be a sequence of bytes-like objects. 
- **os.read**: Read at most n bytes from file descriptor fd.
- **os.sendfile**: Copy count bytes from file descriptor in_fd to file descriptor out_fd starting at offset. Return the number of bytes sent. When EOF is reached return 0.
- **os.set_blocking**: Set the blocking mode of the specified file descriptor. Set the O_NONBLOCK flag if blocking is False, clear the flag otherwise.
- **os.splice**: Transfer count bytes from file descriptor src, starting from offset offset_src, to file descriptor dst, starting from offset offset_dst. 
- **os.readv**: Read from a file descriptor fd into a number of mutable bytes-like objects buffers. Transfer data into each buffer until it is full and then move on to the next buffer in the sequence to hold the rest of the data.
- **os.tcgetpgrp**: Return the process group associated with the terminal given by fd (an open file descriptor as returned by os.open()).
- **os.tcsetpgrp**: Set the process group associated with the terminal given by fd (an open file descriptor as returned by os.open()) to pg.
- **os.ttyname**: Return a string which specifies the terminal device associated with file descriptor fd. If fd is not associated with a terminal device, an exception is raised.
- **os.write**: Write the bytestring in str to file descriptor fd.
- **os.writev**: Write the contents of buffers to file descriptor fd. buffers must be a sequence of bytes-like objects. Buffers are processed in array order. 
- **os.get_terminal_size**: Return the size of the terminal window as (columns, lines), tuple of type terminal_size.
- **os.get_inheritable**: Get the “inheritable” flag of the specified file descriptor (a boolean).
- **os.set_inheritable**: Set the “inheritable” flag of the specified file descriptor.
- **os.get_handle_inheritable**: Get the “inheritable” flag of the specified handle (a boolean).

## Files and Directories

- **os.access**: Use the real uid/gid to test for access to path. 
- **os.chdir**: Change the current working directory to path.
- **os.chflags**: Set the flags of path to the numeric flags. flags may take a combination (bitwise OR) of the following values (as defined in the stat module):
- **os.chmod**: Change the mode of path to the numeric mode. mode may take one of the following values (as defined in the stat module) or bitwise ORed combinations of them:
- **os.chown**: Change the owner and group id of path to the numeric uid and gid. To leave one of the ids unchanged, set it to -1.
- **os.chroot**: Change the root directory of the current process to path.
- **os.fchdir**: Change the current working directory to the directory represented by the file descriptor fd. 
- **os.getcwd**: Return a string representing the current working directory.
- **os.getcwdb**: Return a bytestring representing the current working directory.
- **os.lchflags**: Set the flags of path to the numeric flags, like chflags(), but do not follow symbolic links. 
- **os.lchmod**: Change the mode of path to the numeric mode. If path is a symlink, this affects the symlink rather than the target. 
- **os.lchown**: Change the owner and group id of path to the numeric uid and gid. T
- **os.link**: Create a hard link pointing to src named dst.
- **os.listdir**: Return a list containing the names of the entries in the directory given by path. 
- **os.lstat**: Perform the equivalent of an lstat() system call on the given path. Similar to stat(), but does not follow symbolic links. Return a stat_result object.
- **os.mkdir**: Create a directory named path with numeric mode mode.
- **os.makedirs**: Recursive directory creation function. Like mkdir(), but makes all intermediate-level directories needed to contain the leaf directory.
- **os.mkfifo**: Create a FIFO (a named pipe) named path with numeric mode mode. The current umask value is first masked out from the mode.
- **os.mknod**: Create a filesystem node (file, device special file or named pipe) named path. 
- **os.major**: Extract the device major number from a raw device number (usually the st_dev or st_rdev field from stat).
- **os.minor**: Extract the device minor number from a raw device number (usually the st_dev or st_rdev field from stat).
- **os.makedev**: Compose a raw device number from the major and minor device numbers.
- **os.pathconf**: Return system configuration information relevant to a named file. name specifies the configuration value to retrieve; it may be a string which is the name of a defined system value; these names are specified in a number of standards (POSIX.1, Unix 95, Unix 98, and others). Some platforms define additional names as well. The names known to the host operating system are given in the pathconf_names dictionary. For configuration variables not included in that mapping, passing an integer for name is also accepted.
- **os.pathconf_names**: Dictionary mapping names accepted by pathconf() and fpathconf() to the integer values defined for those names by the host operating system. This can be used to determine the set of names known to the system.
- **os.readlink**: Return a string representing the path to which the symbolic link points. 
- **os.remove**: Remove (delete) the file path. If path is a directory, an OSError is raised. Use rmdir() to remove directories. If the file does not exist, a FileNotFoundError is raised.
- **os.removedirs**: Remove directories recursively.
- **os.rename**: Rename the file or directory src to dst.
- **os.renames**: Recursive directory or file renaming function. 
- **os.replace**: Rename the file or directory src to dst. 
- **os.rmdir**: Remove (delete) the directory path. 
- **os.scandir**: Return an iterator of os.DirEntry objects corresponding to the entries in the directory given by path. 
- **os.stat**: Get the status of a file or a file descriptor. Perform the equivalent of a stat() system call on the given path. 
- **os.statvfs**: Perform a statvfs() system call on the given path. 
- **os.supports_dir_fd**: A set object indicating which functions in the os module accept an open file descriptor for their dir_fd parameter.
- **os.supports_effective_ids**: A set object indicating whether os.access() permits specifying True for its effective_ids parameter on the local platform. 
- **os.access in os.supports_effective_ids**: Currently effective_ids is only supported on Unix platforms; it does not work on Windows.
- **os.supports_fd**: A set object indicating which functions in the os module permit specifying their path parameter as an open file descriptor on the local platform. 
- **os.supports_follow_symlinks**: A set object indicating which functions in the os module accept False for their follow_symlinks parameter on the local platform. 
- **os.symlink**: Create a symbolic link pointing to src named dst.
- **os.sync**: Force write of everything to disk.
- **os.truncate**: Truncate the file corresponding to path, so that it is at most length bytes in size.
- **os.unlink**: Remove (delete) the file path. This function is semantically identical to remove(); the unlink name is its traditional Unix name. 
- **os.utime**: Set the access and modified times of the file specified by path.
- **os.walk**: Generate the file names in a directory tree by walking the tree either top-down or bottom-up. 
- **os.fwalk**: This behaves exactly like walk(), except that it yields a 4-tuple (dirpath, dirnames, filenames, dirfd), and it supports dir_fd.
- **os.memfd_create**: Create an anonymous file and return a file descriptor that refers to it. 
- **os.eventfd**: Create and return an event file descriptor. 
- **os.eventfd_read**: Read value from an eventfd() file descriptor and return a 64 bit unsigned int. The function does not verify that fd is an eventfd().
- **os.eventfd_write**: Add value to an eventfd() file descriptor. value must be a 64 bit unsigned int. The function does not verify that fd is an eventfd().

## Linux extended attributes

- **os.getxattr**: Return the value of the extended filesystem attribute attribute for path. attribute can be bytes or str (directly or indirectly through the PathLike interface). 
- **os.listxattr**: Return a list of the extended filesystem attributes on path. 
- **os.removexattr**: Removes the extended filesystem attribute attribute from path. attribute should be bytes or str (directly or indirectly through the PathLike interface). 
- **os.setxattr**: Set the extended filesystem attribute attribute on path to value. attribute must be a bytes or str with no embedded NULs (directly or indirectly through the PathLike interface).
- **os.abort**: Generate a SIGABRT signal to the current process. On Unix, the default behavior is to produce a core dump; on Windows, the process immediately returns an exit code of 3. 
- **os.add_dll_directory**: Add a path to the DLL search path.


## Process management
- **os.abort**: Generate a SIGABRT signal to the current process. On Unix, the default behavior is to produce a core dump; on Windows, the process immediately returns an exit code of 3.
- **os.add_dll_directory(**: Add a path to the DLL search path.
- **os.execl, os.execle, os.execlp, os.execlpe, os.execv, os.execve, os.execvp, os.execvpe**: These functions all execute a new program, replacing the current process; they do not return. 
- **os._exit**: Exit the process with status n, without calling cleanup handlers, flushing stdio buffers, etc.
- **os.fork**: Fork a child process. Return 0 in the child and the child’s process id in the parent. If an error occurs OSError is raised.
- **os.forkpty**: Fork a child process, using a new pseudo-terminal as the child’s controlling terminal. Return a pair of (pid, fd), where pid is 0 in the child, the new child’s process id in the parent, and fd is the file descriptor of the master end of the pseudo-terminal. For a more portable approach, use the pty module. If an error occurs OSError is raised.
- **os.kill**: Send signal sig to the process pid. Constants for the specific signals available on the host platform are defined in the signal module.
- **os.killpg**: Send the signal sig to the process group pgid.
- **os.nice**: Add increment to the process’s “niceness”. Return the new niceness.
- **os.pidfd_open**: Return a file descriptor referring to the process pid. 
- **os.plock**: Lock program segments into memory. The value of op (defined in <sys/lock.h>) determines which segments are locked.
- **os.popen**: Open a pipe to or from command cmd. The return value is an open file object connected to the pipe, which can be read or written depending on whether mode is 'r' (default) or 'w'. 
- **os.posix_spawn**: Wraps the posix_spawn() C library API for use from Python.
- **os.posix_spawnp**: Wraps the posix_spawnp() C library API for use from Python.
- **os.register_at_fork**: Register callables to be executed when a new child process is forked using os.fork() or similar process cloning APIs. 
- **os.spawnl, os.spawnle, os.spawnlp, os.spawnlpe, os.spawnv, os.spawnve, os.spawnvp, os.spawnvpe**: Execute the program path in a new process.
- **os.startfile**: Start a file with its associated application.
- **os.system**: Execute the command (a string) in a subshell. This is implemented by calling the Standard C function system(), and has the same limitations. Changes to sys.stdin, etc. are not reflected in the environment of the executed command. If command generates any output, it will be sent to the interpreter standard output stream. The C standard does not specify the meaning of the return value of the C function, so the return value of the Python function is system-dependent.
- **os.times**: Returns the current global process times. The return value is an object with five attributes:
- **os.wait**: Wait for completion of a child process, and return a tuple containing its pid and exit status indication: a 16-bit number, whose low byte is the signal number that killed the process, 
- **os.waitid**: Wait for the completion of a child process.
- **os.waitpid**: The details of this function differ on Unix and Windows.
- **os.wait3**: Similar to waitpid(), except no process id argument is given and a 3-element tuple containing the child’s process id, exit status indication, and resource usage information is returned. 
- **os.wait4**: Similar to waitpid(), except a 3-element tuple, containing the child’s process id, exit status indication, and resource usage information is returned. 
- **os.waitstatus_to_exitcode**: Convert a wait status to an exit code.
- **os.WCOREDUMP**: Return True if a core dump was generated for the process, otherwise return False.
- **os.WIFCONTINUED**: Return True if a stopped child has been resumed by delivery of SIGCONT (if the process has been continued from a job control stop), otherwise return False.
- **os.WIFSTOPPED**: Return True if the process was stopped by delivery of a signal, otherwise return False.
- **os.WIFSIGNALED**: Return True if the process was terminated by a signal, otherwise return False.
- **os.WIFEXITED**: Return True if the process exited terminated normally, that is, by calling exit() or _exit(), or by returning from main(); otherwise return False.
- **os.WEXITSTATUS**: Return the process exit status.
- **os.WSTOPSIG**: Return the signal which caused the process to stop.
- **os.WTERMSIG**: Return the number of the signal that caused the process to terminate.

## Interface to the scheduler
- **os.sched_get_priority_min**: Get the minimum priority value for policy. policy is one of the scheduling policy constants above.
- **os.sched_get_priority_max**: Get the maximum priority value for policy. policy is one of the scheduling policy constants above.
- **os.sched_setscheduler**: Set the scheduling policy for the process with PID pid. A pid of 0 means the calling process. policy is one of the scheduling policy constants above. param is a sched_param instance.
- **os.sched_getscheduler**: Return the scheduling policy for the process with PID pid. A pid of 0 means the calling process. The result is one of the scheduling policy constants above.
- **os.sched_setparam**: Set the scheduling parameters for the process with PID pid. A pid of 0 means the calling process. param is a sched_param instance.
- **os.sched_getparam**: Return the scheduling parameters as a sched_param instance for the process with PID pid. A pid of 0 means the calling process.
- **os.sched_rr_get_interval**: Return the round-robin quantum in seconds for the process with PID pid. A pid of 0 means the calling process.
- **os.sched_yield**: Voluntarily relinquish the CPU.
- **os.sched_setaffinity**: Restrict the process with PID pid (or the current process if zero) to a set of CPUs. mask is an iterable of integers representing the set of CPUs to which the process should be restricted.
- **os.sched_getaffinity**: Return the set of CPUs the process with PID pid (or the current process if zero) is restricted to.

## Miscellaneous System Information
- **os.confstr**: Return string-valued system configuration values. name specifies the configuration value to retrieve; it may be a string which is the name of a defined system value; these names are specified in a number of standards (POSIX, Unix 95, Unix 98, and others). Some platforms define additional names as well. The names known to the host operating system are given as the keys of the confstr_names dictionary. For configuration variables not included in that mapping, passing an integer for name is also accepted.
   - os.confstr_names : Dictionary mapping names accepted by confstr()
- **os.cpu_count**: Return the number of CPUs in the system. Returns None if undetermined.
- **os.getloadavg**: Return the number of processes in the system run queue averaged over the last 1, 5, and 15 minutes or raises OSError if the load average was unobtainable.
- **os.sysconf**: Return integer-valued system configuration values. If the configuration value specified by name isn’t defined, -1 is returned.
  - os.sysconf_names:  Dictionary mapping names accepted by sysconf() to the integer values defined for those names by the host operating system. This can be used to determine the set of names known to the system.
- **os.curdir**: The constant string used by the operating system to refer to the current directory. This is '.' for Windows and POSIX. Also available via os.path.
- **os.pardir**: The constant string used by the operating system to refer to the parent directory. This is '..' for Windows and POSIX. Also available via os.path.
- **os.sep**: The character used by the operating system to separate pathname components. This is '/' for POSIX and '\\' for Windows. Note that knowing this is not sufficient to be able to parse or concatenate pathnames — use os.path.split() and os.path.join() — but it is occasionally useful. Also available via os.path.
- **os.altsep**: An alternative character used by the operating system to separate pathname components, or None if only one separator character exists. This is set to '/' on Windows systems where sep is a backslash. Also available via os.path.
- **os.extsep**: The character which separates the base filename from the extension; for example, the '.' in os.py. Also available via os.path.
- **os.pathsep**: The character conventionally used by the operating system to separate search path components (as in PATH), such as ':' for POSIX or ';' for Windows. Also available via os.path.
- **os.defpath**: The default search path used by exec*p* and spawn*p* if the environment doesn’t have a 'PATH' key. Also available via os.path.
- **os.linesep**: The string used to separate (or, rather, terminate) lines on the current platform. This may be a single character, such as '\n' for POSIX, or multiple characters, for example, '\r\n' for Windows. Do not use os.linesep as a line terminator when writing files opened in text mode (the default); use a single '\n' instead, on all platforms.
- **os.devnull**: The file path of the null device. For example: '/dev/null' for POSIX, 'nul' for Windows. Also available via os.path.

## Random numbers
- **os.getrandom**: Get up to size random bytes. The function can return less bytes than requested.
- **os.urandom**: Return a bytestring of size random bytes suitable for cryptographic use.
