# Python Standard Library - os - List of methods (v. 3.11)

Note: Most is copy pasted from the standard library documentation.

## Reference

https://docs.python.org/3/library/os.path.html

## Introduction

Common pathname manipulations (adapts to the system it is running on): 

*This module implements some useful functions on pathnames. **To read or write files see open()**, and **for accessing the filesystem see the os module**.*

## Methods

- **os.path.abspath**: Return a normalized absolutized version of the pathname path. 
- **os.path.basename**: Return the base name of pathname path. 
- **os.path.commonpath**: Return the longest common sub-path of each pathname in the sequence paths. 
- **os.path.commonprefix**: Return the longest path prefix (taken character-by-character) that is a prefix of all paths in list.
- **os.path.dirname**: Return the directory name of pathname path
- **os.path.exists**: Return True if path refers to an existing path or an open file descriptor. 
- **os.path.lexists**: Return True if path refers to an existing path. Returns True for broken symbolic links. 
- **os.path.expanduser**: On Unix and Windows, return the argument with an initial component of ~ or ~user replaced by that user’s home directory.
- **os.path.expandvars**: Return the argument with environment variables expanded. 
- **os.path.getatime**: Return the time of last access of path.
- **os.path.getmtime**: Return the time of last modification of path. 
- **os.path.getctime**: Return the system’s ctime which, on some systems (like Unix) is the time of the last metadata change, and, on others (like Windows), is the creation time for path. 
- **os.path.getsize**: Return the size, in bytes, of path. Raise OSError if the file does not exist or is inaccessible.
- **os.path.isabs**: Return True if path is an absolute pathname. On Unix, that means it begins with a slash, on Windows that it begins with a (back)slash after chopping off a potential drive letter.
- **os.path.isfile**: Return True if path is an existing regular file. 
- **os.path.isdir**: Return True if path is an existing directory. This follows symbolic links, so both islink() and isdir() can be true for the same path.
- **os.path.islink**: Return True if path refers to an existing directory entry that is a symbolic link. Always False if symbolic links are not supported by the Python runtime.
- **os.path.ismount**: Return True if pathname path is a mount point: a point in a file system where a different file system has been mounted.
- **os.path.join**: Join one or more path segments intelligently. The return value is the concatenation of path and all members of *paths.
- **os.path.normcase**: Normalize the case of a pathname.
- **os.path.normpath**: Normalize a pathname by collapsing redundant separators and up-level references so that A//B, A/B/, A/./B and A/foo/../B all become A/B. 
- **os.path.realpath**: Return the canonical path of the specified filename, eliminating any symbolic links encountered in the path (if they are supported by the operating system).
- **os.path.relpath**: Return a relative filepath to path either from the current directory or from an optional start directory.
- **os.path.samefile** : Return True if both pathname arguments refer to the same file or directory. 
- **os.path.sameopenfile**: Return True if the file descriptors fp1 and fp2 refer to the same file.
- **os.path.samestat**: Return True if the stat tuples stat1 and stat2 refer to the same file.
- **os.path.split**: Split the pathname path into a pair, (head, tail) where tail is the last pathname component and head is everything leading up to that.
- **os.path.splitdrive**: Split the pathname path into a pair (drive, tail) where drive is either a mount point or the empty string.
- **os.path.splitext**: Split the pathname path into a pair (root, ext) such that root + ext == path, and the extension, ext, is empty or begins with a period and contains at most one period.
- **os.path.supports_unicode_filenames**: True if arbitrary Unicode strings can be used as file names (within limitations imposed by the file system).
