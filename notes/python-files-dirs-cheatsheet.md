# Python (v. 3.11) - Files, symlinks/hardlinks, directories and paths cheatsheet

- [File](#files)
- [Symlinks/Hardlinks](#symlinks---hardlinks)
- [Directories](#directories)
- [Paths](#paths)

Note: does not include all methods from os, os.path, pathlib or shutil.

## Files

### Tests
- **File exists ?**							
	- `os.path.exists(path)`
	- `Path(mypath).exists()`																

- **Is it a file ?**
	- `os.path.isfile(path)`
	- `Path(mypath).is_file()`

- **Is it the same file?**
	- `os.path.samefile(path1, path2)`
	- `Path(mypath).samefile(other_path)`

### Open a file

```python
with open('workfile', encoding="utf-8") as f:
	read_data = f.read()
```

### Write to a file

```python
with open('workfile', encoding="utf-8") as f:
	f.write('This is a test\n')
```

### Create a file
- **Create an empty file**														
	- `Path(mypath).touch(mode=0o666, exist_ok=True)`

### Update a file
- **Update modification time (touch)**														
	- `Path(mypath).touch(mode=0o666, exist_ok=True)`

### Delete a file
- **Delete a file**
	- `os.remove(path, *, dir_fd=None)`
	- `os.unlink(path, *, dir_fd=None)`
	- `Path(mypath).unlink(missing_ok=False)`

### Copy a file
- **Copy a file and preserve some metadata**													
	- **`shutil.copy2(src, dst, *, follow_symlinks=True)`**
- **Copy a file without metadata**															
	- `shutil.copy(src, dst, *, follow_symlinks=True)`
- **Copy the file permissions**																	
	- `shutil.copymode(src, dst, *, follow_symlinks=True)`
- **Copy a file with permission bits, last access time, last modification time, and flags**		
	- `shutil.copystat(src, dst, *, follow_symlinks=True)`
- **Copy a file object**																	
	- `shutil.copyfileobj(fsrc, fdst[, length])`

### Move - rename - replace a file
- **Move a file**
	- `shutil.move(src, dst, copy_function=copy2)`
- **Rename a file**
	- `Path(mypath).rename(target)`
	- `os.rename(src, dst, *, src_dir_fd=None, dst_dir_fd=None)`
- **Rename recursively**
	- `os.renames(old, new)`
- **Replace a file**
	- `os.replace(src, dst, *, src_dir_fd=None, dst_dir_fd=None)`
	- `Path(mypath).replace(target)`

### Get a file name
- **File name with extension**:
	- `os.path.basename(path)`
	- `PurePath(mypath).name`
- **Split the filename and the extension**:
	- `os.path.splitext(path)`
	- Filename: `PurePath(mypath).stem`
	- Extension: `PurePath(mypath).suffix`

### Recursive operations
- **Copy recursively** 																		
	- `shutil.copytree(src, dst, symlinks=False, ignore=None, copy_function=copy2, ignore_dangling_symlinks=False, dirs_exist_ok=False)`
- **Delete recursively**																	
	- `shutil.rmtree(path, ignore_errors=False, onerror=None, *, dir_fd=None) [Note: use ignore_errors=True]`

### Archives
- **Make a zip or tar or gztar archive**
	- `shutil.make_archive(base_name, format[, root_dir[, base_dir[, verbose[, dry_run[, owner[, group[, logger]]]]]]])`
- **Unpack the archive**
	- `shutil.unpack_archive(filename[, extract_dir[, format]])`

## Symlinks - Hardlinks

### Symlinks
- **Is a symlink ?**																	
	- `os.path.islink(path)`
	- `Path(mypath).is_symlink()`

- **Create a symlink**
	- `os.symlink(src, dst, target_is_directory=False, *, dir_fd=None)`
	- `Path(mypath).symlink_to(target, target_is_directory=False)`			

### Hardlinks																	
- **Is a hardlink ?**
	- `os.link(src, dst, *, src_dir_fd=None, dst_dir_fd=None, follow_symlinks=True)`
	- `Path(mypath).hardlink_to(target)`

### Path
- **Returns the path to which the symbolic link points**
	- `os.readlink(path, *, dir_fd=None)`
	- `Path(mypath).readlink()`

## Directories

### Tests
- **is it a directory ?**																
	- `os.path.isdir(path)`
	- `Path(mypath).is_dir()`
- **is is an absolute path ?**
	- `os.path.isabs(path)`
	- `PurePath(mypath).is_absolute()`

### Create a directory
- **Create a directory**
	- `os.mkdir(path, mode=0o777, *, dir_fd=None)`
	- `Path(mypath).mkdir(mode=0o777, parents=False, exist_ok=False)` [Note: use exist_ok=True]
- **Create a directory with his parents**
    - `os.makedirs(name, mode=0o777, exist_ok=False)` [Note: use exist_ok=True]
	- `Path(mypath).mkdir(mode=0o777, parents=False, exist_ok=False)`

### Get the directory name of the file's parent
- **Parent directory**:
	- `os.path.dirname(path)`
	- `PurePath(mypath).parent`

### Delete a directory
Note: directory must be empty
  - `os.rmdir(path, *, dir_fd=None)`
  - `Path(mypath).rmdir()`

### Move - rename - replace a directory
- **Move a directory**
	- `shutil.move(src, dst, copy_function=copy2)`
- **Rename a directory**
	- `Path(mypath).rename(target)`
	- `os.rename(src, dst, *, src_dir_fd=None, dst_dir_fd=None)`
- **Rename recursively**
	- `os.renames(old, new)`
- **Replace a directory**
	- `os.replace(src, dst, *, src_dir_fd=None, dst_dir_fd=None)`
	- `Path(mypath).replace(target)`

### List the content of a directory
- **List the content**
	- `os.listdir(path='.')`
	- `Path.iterdir()`

## Paths

### Get the paths
- **Current working directory**
	- `os.getcwd()`
	- `Path(mypath).cwd()`
- **Get home directory**
	- `os.path.expanduser(path)`
	- `Path(mypath).expanduser()`
	- `Path(mypath).home()`
- **Absolute path**
	- `os.path.abspath(path)`
    	- `Path(mypath).absolute()`
- **Real path**
	- `os.path.realpath()`
	- `Path(mypath).resolve(strict=False)`
- **Path relative to another**
	- `os.path.realpath(path, *, strict=False)`
	- `PurePath(mypath).relative_to(*other)`

### Join and normalize paths

- **Join several paths**
	- `os.path.join(path, *paths)`
	- `PurePath(mypath).joinpath(*other)`
- **Normalize a path (by collapsing redundant separators and up-level references)**
	- `os.path.normpath(path)`

### Permissions - Statistics
- **Get the statistics and permissions**
	- `os.stat(path, *, dir_fd=None, follow_symlinks=True)`
	- `Path(mypath).stat()`
	- [os.stat details](https://docs.python.org/3/library/os.html#os.stat)
- **Get the owner's names**
	- `Path(mypath).owner()`
- **Get the group's name**
	- `Path(mypath).group()`
- **Change the owner and group with a user name and a group name**
	- `shutil.chown(path, user=None, group=None)`
- **Change the owner and group with a user ID and group ID**
	- `os.chown(path, uid, gid, *, dir_fd=None, follow_symlinks=True)`
- **Change the permissions with a mode**
	- `os.chmod(path, mode, *, dir_fd=None, follow_symlinks=True)`
	- `Path(mypath).chmod(Path.chmod(mode, *, follow_symlinks=True)`
