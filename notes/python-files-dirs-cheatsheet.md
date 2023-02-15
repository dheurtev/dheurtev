# Python (v. 3.11) - Files, symlinks/hardlinks and directories cheatsheet

[File](#files)
[Symlinks/Hardlinks](#symlinks---hardlinks)
[Directories](#directories)

## Files

### Test
- **File exists ?**							
	- `os.path.exists(path)`
	- `Path(mypath).exists()`																

- **Is a file ?**
	- `os.path.isfile(path)`
	- `Path(mypath).is_file()`

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
- **Replace a file**
	- `os.replace(src, dst, *, src_dir_fd=None, dst_dir_fd=None)`
	- `Path(mypath).replace(target)`

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
### Permissions
- **Change user, group of a file with user name and group name**
	- `shutil.chown(path, user=None, group=None)`

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






