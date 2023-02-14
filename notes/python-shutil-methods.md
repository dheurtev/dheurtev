# Python Standard Library (v. 3.11) - shutil - List of Methods

Note: Most is copy pasted from the standard library documentation.

## Reference

https://docs.python.org/3/library/shutil.html

## Introduction

*The shutil module offers a number of **high-level operations on files and collections of files**. In particular, functions are provided which support file copying and removal. For operations on individual files, see also the os module.*

## Methods

[Comparison of Shutil copy methods](https://stackoverflow.com/questions/123198/how-to-copy-files)
| Function           | Copies   | Copies	    | Uses 	       | Destination       |
|                    | metadata | permissions | file object  | may be directory  |
|--------------------|----------|-------------|--------------|-------------------|
| shutil.copy	       |   No	    |  **Yes**    |      No	     |  **Yes**          |
| shutil.copyfile	   |   No	    |    No       |      No      | 	  No             |
| shutil.copy2	     | **Yes**	|  **Yes**    |	     No      |  **Yes**          |
| shutil.copyfileobj |	 No     |	   No	      |    **Yes**   |    No             |

- **shutil.copyfileobj**: Copy the contents of the file-like object fsrc to the file-like object fdst.
- **shutil.copyfile**: Copy the contents (no metadata) of the file named src to a file named dst and return dst in the most efficient way possible.
- **shutil.copymode**: Copy the permission bits from src to dst. The file contents, owner, and group are unaffected.
- **shutil.copystat**: Copy the permission bits, last access time, last modification time, and flags from src to dst.
- **shutil.copy**: Copies the file src to the file or directory dst.
- **shutil.copy2**: Identical to copy() except that copy2() also attempts to preserve file metadata.
- **shutil.ignore_patterns**: This factory function creates a function that can be used as a callable for copytree()'s ignore argument, ignoring files and directories that match one of the glob-style patterns provided. See the example below.
- **shutil.copytree**: Recursively copy an entire directory tree rooted at src to a directory named dst and return the destination directory.
- **shutil.rmtree**: Delete an entire directory tree; path must point to a directory (but not a symbolic link to a directory). If ignore_errors is true, errors resulting from failed removals will be ignored; if false or omitted, such errors are handled by calling a handler specified by onerror or, if that is omitted, they raise an exception.
- **shutil.move**: Recursively move a file or directory (src) to another location (dst) and return the destination.
- **shutil.disk_usage**: Return disk usage statistics about the given path as a named tuple with the attributes total, used and free, which are the amount of total, used and free space, in bytes. path may be a file or a directory.
- **shutil.chown**: Change owner user and/or group of the given path.
- **shutil.which**: Return the path to an executable which would be run if the given cmd was called. If no cmd would be called, return None.
- **shutil.make_archive**: Create an archive file (such as zip or tar) and return its name. [zip, tar, gztar, bztar, xztar]
- **shutil.get_archive_formats**: Return a list of supported formats for archiving. Each element of the returned sequence is a tuple (name, description).
- **shutil.register_archive_format**: Register an archiver for the format name.
- **shutil.unregister_archive_format**: Remove the archive format name from the list of supported formats.
- **shutil.unpack_archive**: Unpack an archive. filename is the full path of the archive.
- **shutil.register_unpack_format**: Registers an unpack format. name is the name of the format and extensions is a list of extensions corresponding to the format, like .zip for Zip files.
- **shutil.unregister_unpack_format**: Unregister an unpack format. name is the name of the format.
- **shutil.get_unpack_formats**: Return a list of all registered formats for unpacking. Each element of the returned sequence is a tuple (name, extensions, description).
