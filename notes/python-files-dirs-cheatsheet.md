# Python (v. 3.11) - Files and directories cheatsheet

## Files

### Test
- **File exists ?**							
	- `os.path.exists(path)`
	- `Path(mypath).exists()`																

- **Is a file ?**
	- `os.path.isfile(path)`
	- `Path(mypath).is_file()`

### Open a file

`py **with open('workfile', encoding="utf-8") as f:**
	**read_data = f.read()**`

### Write to a file

`py**with open('workfile', encoding="utf-8") as f:**
	**f.write('This is a test\n')**`






## Directories




## Symlinks/Hardlinks

### Symlinks
- **Is a symlink ?**																	
	- os.path.islink(path)
	- Path(mypath).is_symlink()

- **Create a symlink**
	- os.symlink(src, dst, target_is_directory=False, *, dir_fd=None)
	- Path(mypath).symlink_to(target, target_is_directory=False)			

### Hardlinks																	
- **Is a hardlink ?**
	- os.link(src, dst, *, src_dir_fd=None, dst_dir_fd=None, follow_symlinks=True)
	- Path(mypath).hardlink_to(target)

### Path
- **Returns the path to which the symbolic link points**
	- os.readlink(path, *, dir_fd=None)
	- Path(mypath).readlink()
