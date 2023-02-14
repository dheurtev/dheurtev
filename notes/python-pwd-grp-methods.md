# Python Standard Library (v. 3.11) - pwd/grp - List of Methods

Note: Most is copy pasted from the standard library documentation - Licensed :Python Software Foundation License Version 2.

## Reference

- pwd: https://docs.python.org/3/library/pwd.html
- grp: https://docs.python.org/3/library/grp.html

## PWD - Password database

### Introduction

*This module provides access to the **Unix user account and password database**. It is available on all Unix versions.*

Password database entries are reported as a tuple-like object, whose attributes correspond to the members of the passwd structure (Attribute field below, see <pwd.h>):

| Index | Attribute | Meaning                     |
|-------|-----------|-----------------------------|
|   0   | pw_name   | Login name                  |
|   1   | pw_passwd | Optional encrypted password |
|   2   | pw_uid    | Numerical user ID           |
|   3   | pw_gid    | Numerical group ID          |
|   4   | pw_gecos  | User name or comment field  |
|   5   | pw_dir    | User home directory         |
|   6   | pw_shell  | User command interpreter    |

### Methods

- **pwd.getpwuid**: Return the password database entry for the given numeric user ID.
- **pwd.getpwnam**: Return the password database entry for the given user name.
- **pwd.getpwall**: Return a list of all available password database entries, in arbitrary order.

## GRP - Group database

### Introduction

*This module provides access to the **Unix group database**. It is available on all Unix versions.*

| Index | Attribute | Meaning                                     |
|-------|-----------|---------------------------------------------|
|   0   | gr_name   | the name of the group                       |
|   1   | gr_passwd | the (encrypted) group password; often empty |
|   2   | gr_gid    | the numerical group ID                      |
|   3   | gr_mem    | all the group member’s user names           |

### Methods

- **grp.getgrgid**: Return the group database entry for the given numeric group ID. KeyError is raised if the entry asked for cannot be found.
- **grp.getgrnam**: Return the group database entry for the given group name. KeyError is raised if the entry asked for cannot be found.
- **grp.getgrall**: Return a list of all available group entries, in arbitrary order.
