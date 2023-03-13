---
name: فرم گزارش آزمایش سوم
about: برای نوشتن گزارش آزمایشگاه از این تمپلیت استفاده کنید
title: Session 3 Report
labels: documentation
assignees: amirhossein1376

---

Team Name: `[FILL HERE]`

Student Name of member 1: `[FILL HERE]`
Student No. of member 1: `[FILL HERE]`

Student Name of member 2: `[FILL HERE]`
Student No. of member 2: `[FILL HERE]`

- [ ] Read Session Contents.

### Section 3.3.1
- [ ] Investigate the /proc/ directory
    1. [ ] `[FILL HERE with an image of files in /proc/ directories. Use ls command.]`

### Section 3.3.2

- [ ] Do 5 subtasks from 1 to 5:
    1. [ ] `[FILL HERE with the content of /proc/version. Use cat command.]`
    1. [ ] `[FILL HERE with the content of two files with non-numeric name other thatn /proc/version.]`
    1. [ ] `[FILL HERE with the program you write for this part (see experiment guide for information).]`
    1. [ ] `[FILL HERE with screen capture from your programs execution.]`
    1. [ ] `[FILL HERE with description about, what happens if you try to write a sentence in to /proc/version.]`

## Section 3.3.3

- [ ] Write (in English or Persian) about each file in /proc/(PID) directory:
    1. `[FILL HERE with description about cmdline]`
    1. `[FILL HERE with description about environ]`
    1. `[FILL HERE with description about stat]`
    1. `[FILL HERE with description about status]`
    1. `[FILL HERE with description about statm]`
    1. `[FILL HERE with description about cwd]`
    1. `[FILL HERE with description about exe]`
    1. `[FILL HERE with description about root]`

- [ ] Place your script for shwoing PID of running porcesses and their name here:
    - [ ] `[FILL HERE with your script]`

- [ ] Place your source code for a program that shows details of a program by receiving PID:
    - [ ] `[FILL HERE with your source code]`

### Section 3.3.4

- [ ] Write (in English or Persian) about each file in /proc/ directory:
    1. `[FILL HERE with description about meminfo]`
    1. `[FILL HERE with description about version]`
    1. `[FILL HERE with description about uptime]`
    1. `[FILL HERE with description about stat]`
    1. `[FILL HERE with description about mount]`
    1. `[FILL HERE with description about net directory (or file)]`
    1. `[FILL HERE with description about loadavg]`
    1. `[FILL HERE with description about interrupts]`
    1. `[FILL HERE with description about ioports]`
    1. `[FILL HERE with description about filesystem]`
    1. `[FILL HERE with description about cpuinfo]`
    1. `[FILL HERE with description about cmdline]`

- [ ] Place your source code for a program that shows details of processor:
    - [ ] `[FILL HERE with your source code]`

- [ ] Place your source code for a program that shows details of memory management sub-system:
    - [ ] `[FILL HERE with your source code]`

- [ ] Write your description about five important files at /proc/sys/kernel:
    - [ ] `[hostname: This file contains the hostname of the system. It can be used to view or change the hostname of the system.]`
    - [ ] `[osrelease: This file contains the version number of the Linux kernel that is currently running on the system]`
    - [ ] `[panic: This file controls what the kernel does when it encounters a critical error that could lead to a system crash. By default, the kernel will reboot the system if it encounters a critical error. However, this file can be used to change the behavior and set it to panic, halt, or ignore the error.]`
    - [ ] `[core_pattern: This file specifies the name and location of the core dump file that is generated when a program crashes. By default, the core dump file is named core and is located in the current working directory. However, this file can be used to change the name and location of the core dump file.]`
    - [ ] `[sysrq: This file controls the behavior of the Magic SysRq key. The Magic SysRq key is a key combination that can be used to send various commands directly to the kernel, even if the system is unresponsive or in a hung state. The contents of this file can be used to enable or disable certain commands that are available through the Magic SysRq key.]`

- [ ] Write your description about /proc/self file
    - [ ] `[In the /proc directory of a Linux system, the self directory is a symbolic link to the directory corresponding to the currently executing process. It contains information about the currently running process in the form of various files.

When a process reads or writes to a file in the /proc/self directory, it is actually reading or writing to the corresponding file in its own /proc directory. This means that a process can use the self directory to access information about itself or to modify its own behavior.

For example, a process can use the /proc/self/cmdline file to get the command line arguments that were used to start the process. This can be useful for debugging or for writing scripts that need to know how a particular process was started.

Similarly, a process can use the /proc/self/exe file to get the full path of its own executable file. This can be useful for determining the location of a binary file that is currently running.

The /proc/self directory can also be used to modify the behavior of the current process. For example, a process can use the /proc/self/oom_adj file to adjust its Out Of Memory (OOM) score, which determines how likely it is to be killed by the OOM killer when the system is running out of memory.

Overall, the /proc/self directory provides a way for a process to access information about itself and to modify its own behavior, which can be useful in a variety of contexts.]`


## Source Code Submission

please submit all your codes in a zip file

 - [ ] `Zip File HERE`
