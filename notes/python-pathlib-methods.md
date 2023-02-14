# Python Standard Library (v.3.11) - pathlib - List of methods

## Reference

https://docs.python.org/3/library/pathlib.html

## Introduction

*"This module offers classes representing **filesystem paths** with semantics appropriate for different operating systems"*

`py from pathlib import Path`

`p = Path('/')`

## Methods

[Table of correspondence between os/os.path and pathlib ](https://docs.python.org/3/library/pathlib.html?highlight=path#module-pathlib)

| os and os.path           | pathlib                                 |
|--------------------------|-----------------------------------------|
| os.path.abspath()        | Path.absolute()                         |
| os.path.realpath()       | Path.resolve()                          |
| os.chmod()               | Path.chmod()                            |
| os.mkdir()               | Path.mkdir()                            |
| os.makedirs()            | Path.mkdir()                            |
| os.rename()              | Path.rename()                           |
| os.replace()             | Path.replace()                          |
| os.rmdir()               | Path.rmdir()                            |
| os.remove(), os.unlink() | Path.unlink()                           |
| os.getcwd()              | Path.cwd()                              |
| os.path.exists()         | Path.exists()                           |
| os.path.expanduser()     | Path.expanduser() and Path.home()       |
| os.listdir()             | Path.iterdir()                          |
| os.path.isdir()          | Path.is_dir()                           |
| os.path.isfile()         | Path.is_file()                          |
| os.path.islink()         | Path.is_symlink()                       |
| os.link()                | Path.hardlink_to()                      |
| os.symlink()             | Path.symlink_to()                       |
| os.readlink()            | Path.readlink()                         |
| os.path.relpath()        | PurePath.relative_to()                  |
| os.stat()                | Path.stat(), Path.owner(), Path.group() |
| os.path.isabs()          | PurePath.is_absolute()                  |
| os.path.join()           | PurePath.joinpath()                     |
| os.path.basename()       | PurePath.name                           |
| os.path.dirname()        | PurePath.parent                         |
| os.path.samefile()       | Path.samefile()                         |
| os.path.splitext()       | PurePath.stem and PurePath.suffix       |

### PurePath

- **PurePath.parts** : Path’s various components
- **PurePath.drive** : Drive letter or name
- **PurePath.root** : Local or global root
- **PurePath.anchor** : Concatenation of the drive and root
- **PurePath.parents** : Logical ancestors of the path
- **PurePath.parent** : Logical parent of the path
- **PurePath.name** : Final path component, excluding the drive and root, if any
- **PurePath.suffix** : File extension of the final component, if any
- **PurePath.suffixes** : A list of the path’s file extensions
- **PurePath.stem** : Final path component, without its suffix
- **PurePath.as_posix** : POSIX : the path with forward slashes (/)
- **PurePath.as_uri** : Path as a file URI (file:///)
- **PurePath.is_absolute** : Whether the path is absolute or not
- **PurePath.is_relative_to** : Whether or not this path is relative to the other path
- **PurePath.is_reserved** : PureWindowsPath: True if considered reserved, False otherwise. PurePosixPath: always False
- **PurePath.joinpath** : Combining the path with each of the other arguments
- **PurePath.match**: Match this path against the provided glob-style pattern. True if successful, else False
- **PurePath.relative_to** : Version of this path relative to the path represented by other
- **PurePath.with_name** : New path with the name changed
- **PurePath.with_stem** : New path with the stem changed
- **PurePath.with_suffix** : New path with the suffix changed

### Path

- **Path.cwd** : New path object representing the current directory (os.getcwd())
- **Path.home** : New path object representing the user’s home directory (os.path.expanduser() ~ construct)
- **Path.stat** : os.stat_result object containing information about this path, like os.stat()
- **Path.chmod** : Change file mode and permissions, like os.chmod()
- **Path.exists** : Whether the path points to an existing file or directory
- **Path.expanduser** : New path with expanded ~ and ~user constructs, as returned by os.path.expanduser() 
- **Path.glob** : Glob the given relative pattern in the path directory. Yield all matching files
- **Path.group** : Name of the group owning the file                                                          
- **Path.is_dir** : Does the path point to a directory (or a symbolic link pointing to a directory) ?
- **Path.is_file** : Does the path point to a regular file (or a symbolic link pointing to a regular file) ?
- **Path.is_mount** : Does the path point to a mount point ?
- **Path.is_symlink** : Does the path point to a symbolic link ?
- **Path.is_socket** : Does the path point to a Unix socket (or a symbolic link pointing to a Unix socket) ?
- **Path.is_fifo** : Does the path point to a FIFO (or a symbolic link pointing to a FIFO) ?
- **Path.is_block_device** : Does the path point to a block device (or a symbolic link pointing to a block device) ?
- **Path.is_char_device** : Does the path point to a character device (or a symbolic link pointing to a character device) ?
- **Path.iterdir** : When the path points to a directory, yield path objects of the directory contents
- **Path.lchmod** : Like Path.chmod() but, if the path points to a symbolic link, the symbolic link’s mode is changed rather than its target’s
- **Path.lstat** : Like Path.stat() but, if the path points to a symbolic link, return the symbolic link’s information rather than its target’s
- **Path.mkdir** : Create a new directory at this given path 
- **Path.open** : Open the file pointed to by the path, like the built-in open() function does
- **Path.owner** : Return the name of the user owning the file.
- **Path.read_bytes** : Returns the binary contents of the pointed-to file as a bytes object
- **Path.read_text** : Returns the decoded contents of the pointed-to file as a string: 
- **Path.readlink** : Returns the path to which the symbolic link points (as returned by os.readlink())
- **Path.rename** : Rename this file or directory to the given target, and return a new Path instance pointing to target.
- **Path.replace** : Rename this file or directory to the given target, and return a new Path instance pointing to target.
- **Path.absolute** : Make the path absolute, without normalization or resolving symlinks.
- **Path.resolve** : Make the path absolute, resolving any symlinks.
- **Path.rglob** : This is like calling Path.glob() with “**/” added in front of the given relative pattern
- **Path.rmdir** : Remove this directory. The directory must be empty.
- **Path.samefile** : Return whether this path points to the same file as other_path, which can be either a Path object, or a string.
- **Path.symlink_to** : Make this path a symbolic link to target.
- **Path.hardlink_to** : Make this path a hard link to the same file as target.
- **Path.link_to** : Make target a hard link to this path.
- **Path.touch** : Create a file at this given path. Updates modification time if exists (with exist_ok=True)
- **Path.unlink** : Remove this file or symbolic link. If the path points to a directory, use Path.rmdir() instead.
- **Path.write_bytes** : Open the file pointed to in bytes mode, write data to it, and close the file
- **Path.write_text** : Open the file pointed to in text mode, write data to it, and close the file
