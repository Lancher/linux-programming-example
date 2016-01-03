## Linux programming in C

#### Introduction :

Some simple linux programming codes.

--

#####  Memory and Allocaton:

- Memory alignment please refer to `Sven-Hendrik Haase - Alignment in C`.

| Code | Descriptions  |
| --- | --- |
| [malloc_free_sbrk.c](src/malloc_free_sbrk.c) | Observe how a program heap size changed by mallocing and freeing memory. |
| [memory_align.c](src/memory_align.c) | Demonstrate how "posix_memalign()" work. |

--

##### Users and Groups:

- Retrieve info in `/etc/passwd` and `/etc/group`.

| Code | Descriptions  |
| --- | --- |
| [users_groups.c](src/users_groups.c) | Fetch users and groups info in `/etc/passwd` and `/etc/group`. |

--

##### Process Credentials:

- Relation between real user ID(real uid, or ruid), the effective user ID (effective uid, or euid), and the saved user ID (saved uid, or suid).

- Please refer to paper `Setuid Demystified` for more details.

| Code | Descriptions  |
| --- | --- |
| [process_cred.c](src/process_cred.c) | Observe a process's real UID, effective UID and save UID.|

--

##### Time:

- Conversions between `time()`, `gmtime()`, `localtime()`, `asctime()`, `ctime()` and `mktime().`

- Process Time is divide to `User CPU time`(the time of the program access CPU) and `System CPU Time`(the time of kernel system call, page faults..).

| Code | Descriptions  |
| --- | --- |
| [time.c](src/time.c) | Time functions.|
| [process_time.c](src/process_time.c) | Get the User CPU Time and System CPU Time.|

--

##### File I/O:

- The `read()` and “write()` system calls don’t directly initiate disk access. Instead, they simply copy data between a user-space buffer and a buffer in the kernel buffer cache.


| Code | Descriptions  |
| --- | --- |
| [direct_io.c](src/direct_io.c) | Using `O_DIRECT` to bypass the buffer cache.|
| [file_info.c](src/file_info.c) | Get file flags and permission.|

--


