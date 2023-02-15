# Python (v. 3.11) - Files and directories cheatsheet

## Files





## Directories




## Symlinks/Hardlinks

### Symlinks
is symlink																	os.path.islink(path)
																						Path(mypath).is_symlink()

Create a symlink														os.symlink(src, dst, target_is_directory=False, *, dir_fd=None)
																						Path(mypath).symlink_to(target, target_is_directory=False)			

### Hardlinks																	
is hardlink																	os.link(src, dst, *, src_dir_fd=None, dst_dir_fd=None, follow_symlinks=True)
																						Path(mypath).hardlink_to(target)

### Path
Returns the path to which the symbolic link points										os.readlink(path, *, dir_fd=None)
								                          														Path(mypath).readlink()
