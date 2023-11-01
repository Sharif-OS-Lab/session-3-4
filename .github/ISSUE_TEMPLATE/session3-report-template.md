name: فرم گزارش آزمایش سوم
about: برای نوشتن گزارش آزمایشگاه از این تمپلیت استفاده کنید
title: Session 3 Report
labels: documentation
assignees: amirhossein1376

---

Team Name: `98170849-98109729`

Student Name of member 1: `Sara Zahedi`
Student No. of member 1: `Paniz Halvachi`

Student Name of member 2: `98170849`
Student No. of member 2: `98109729`

- [ ] Read Session Contents.

### Section 3.3.1
- [ ] Investigate the /proc/ directory
    1. [ ] `[FILL HERE with an image of files in /proc/ directories. Use ls command.]`
    2. ![20231031_214806](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/06a4ec67-533e-4a08-a8be-fd944206516d)


### Section 3.3.2

- [ ] Do 5 subtasks from 1 to 5:
    1. [ ] `[FILL HERE with the content of /proc/version. Use cat command.]`
    2. sara-paniz@98170849-98109729:/procs cat version
Linux version 5.4.0-125-generic (buildd@1cy02-amd64-083) (gcc version 9.4.0 (Ubuntu 9.4.0-1ubuntu1 20.04.1)) #141-Ubuntu SMP Wed Aug 10 13:42:03 UTC 2022
    1. [ ] `[FILL HERE with the content of two files with non-numeric name other thatn /proc/version.]`
    2. sara-paniz@98170849-98109729:/procs cat uptime
1399.19 179.27

First Value: Total number of seconds the system has been up since it was last booted
Second Value: Amount of time the system has been idle in seconds
       
    4. sara-paniz@98170849-98109729:/procs cat key-users
0:    67 66/66 52/1000000 1059/25000000
100:    1    1/1 1/200    9/20000
101:    1    1/1 1/200    9/20000
102:    1    1/1 1/200    9/20000
1000:    3    3/3 3/200    37/20000

First Value: Key type identifier.
Second Value: Number of keys of that type that are currently instantiated.
Third Value: Quota of keys of that type.
Fourth Value: Number of keys that have been created but not yet instantiated.
Fifth Value: Quota of keys that have been created but not yet instantiated.

    1. [ ] `[FILL HERE with the program you write for this part (see experiment guide for information).]`

```
#include <bits/stdc++.h>
using namespace std;

int main(){
    fstream file;
    file.open("/proc/version",ios::in);
    if(!file.is_open()){
        perror("error in reading");
        return 1;
    }
    fstream file2;
    file2.open("./Linux Version.txt",ios::out | ios::app);
    if(!file2.is_open()){
        perror("error in writing");
        return 1;
    }
    string line;
    while (!file.eof()){
        getline(file,line);
        file2 << line;
    }
return 0;
}
```
    
    1. [ ] `[FILL HERE with screen capture from your programs execution.]`
    ![1](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/69b749eb-5509-4346-8eb9-332eae79f394)

    1. [ ] `[FILL HERE with description about, what happens if you try to write a sentence in to /proc/version.]`
    This file is read only so we cannot write anything
    ![2](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/0b6c7702-846e-4f88-b0c4-881e828e1ee7)


## Section 3.3.3

- [ ] Write (in English or Persian) about each file in /proc/(PID) directory:
- [ ]     2. ![3](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/8b8b2c4c-7289-40b5-b728-4cf8941e6e2e)

    1. `[FILL HERE with description about cmdline]`
    cmdline: This is a read-only file which contains the arguments of commandlines for running the processor
![10](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/36af713b-e8da-48e0-b321-1509b0d36ce5)


    1. `[FILL HERE with description about environ]`
    2. environ: This file contains the initial environment variables.
    3. ![11](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/9e28dd1a-3131-4c48-b9cf-e213a868caa1)



    1. `[FILL HERE with description about stat]`
    3. This file provides all info about processor status.
    4. ![12](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/a33deaef-23d2-490d-9c05-7740dc80e39c)


    1. `[FILL HERE with description about status]`
    2.  This file shows the status info of process.
    3.  ![13](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/f99bf72c-b3e2-4834-a5ce-9f81d53e506d)



    1. `[FILL HERE with description about statm]`
    2. This file presents the information of allocated memory to processor
    3. ![14](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/b314e784-3817-4b01-9fe7-d4028c9ddb86)



    1. `[FILL HERE with description about cwd]`
    2. This provides the current working directory
    3. ![15](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/7847fcb8-3509-4d30-8508-2bde572a2850)

     
    1. `[FILL HERE with description about exe]`
    2. This is the executable fule
    3. ![16](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/5d6d705b-e669-4e7a-8ddb-aa2ab740948c)

  
    
    1. `[FILL HERE with description about root]`
    2. It shows the path of root directory
    3. ![17](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/ecbb0035-bc48-435f-8f44-8226c6208680)


- [ ] Place your script for shwoing PID of running porcesses and their name here:
    - [ ] `[FILL HERE with your script]`
   ![code](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/c88e060e-637a-4cba-8f42-0378d945ce82)

- [ ] Place your source code for a program that shows details of a program by receiving PID:
    - [ ] `[FILL HERE with your source code]`
     ![code1](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/5a44181f-fe1c-47f3-8547-e07be9229a49)



          ![18](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/b6c6a953-e361-4ef8-a82a-bbf9c4fd4da5)


### Section 3.3.4

- [ ] Write (in English or Persian) about each file in /proc/ directory:
    1. `[FILL HERE with description about meminfo]`
    2. اطلاعات مختلف درباره حافظه سیستم مثل حجم حافظه و حافظه آزاد و ...
       
    1. `[FILL HERE with description about version]`
    2. اطلاعات درباره نسخه هسته لینوکس به ما ارائه میکند مثل نسحه هسته
       
    1. `[FILL HERE with description about uptime]`
    2. زمانی که سیتم روشن است و زمانی که سیستم درحال اجراست.
       
    1. `[FILL HERE with description about stat]`
    2. بررسی و اطلاعات درباره پردازنده مثل idle بودن
    1. `[FILL HERE with description about mount]`
    2. اطلاعات در مورد فایل سیستم و نقاط مونت شده در سیستم
    1. `[FILL HERE with description about net directory (or file)]`
    2. اطلاعات درباره شبکه ها و اتصالات
    1. `[FILL HERE with description about loadavg]`
    2. بار سیستم در زمان مشخص
    1. `[FILL HERE with description about interrupts]`
    2. اطلاعات وقفه ها در سیستم
    1. `[FILL HERE with description about ioports]`
    2. اطلاعات پورت های ورودی و خروجی
    1. `[FILL HERE with description about filesystem]`
    2. نوع فایل سیستم هایی که سیستم پشتیبانی میکند
    1. `[FILL HERE with description about cpuinfo]`
    2. اطلاعات درباره پردازه های موجود د سیستم مثل نوع پردازنده
    1. `[FILL HERE with description about cmdline]`
    2. پارامترهای دستور خط فرمانی

- [ ] Place your source code for a program that shows details of processor:
    - [ ] `[FILL HERE with your source code]`
    - [ ] ![21](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/c52e42dd-3c10-4eb5-bc22-abbf3dbe86e4)


- [ ] Place your source code for a program that shows details of memory management sub-system:
    - [ ] `[FILL HERE with your source code]`
    - [ ]![23](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/81d9578c-2dea-422f-a732-1029819f05bd)




- [ ] Write your description about five important files at /proc/sys/kernel:
    - [ ] `[FILL HERE with your descript for 1st file]`
    - [ ] osrelease:
    - [ ] کاربرد این فایل آن است که نسخه هسته لینوکس را که درحال اجرا است را نشان میدهد و اطلاعات آن به صورت خودکار آپدیت میشود و نمیتوان آن را تغییر داد.
    - [ ] `[FILL HERE with your descript for 2nd file]`
    - [ ] Panic:
    - [ ] تعداد ثانیه هایی که هسته باید بعد از یک kernel panic صبر کند تا ریست شود را نشان میدهد.
    - [ ] `[FILL HERE with your descript for 3rd file]`
    - [ ] printk:
    - [ ] این فایل کنترل میکند که پیام های خروجی هسته چگونه نمایش داده شوند. در این فایل 4 مقدار وجود دارد و هرکدام نشان دهنده یک لول است که خطا در آن قرار دارد.
    - [ ] `[FILL HERE with your descript for 4th file]`
    - [ ] ostype:
    - [ ] این فایل نوع سیستم عامل را مشخص میکند مثلا لینوکس. اطلاعات این فایل قابل تغییر نیست و خودش آپدیت میشود.
    - [ ] `[FILL HERE with your descript for 5th file]`
    - [ ] hostname:
    - [ ] این فایل نام میزبان سیستم را ذخیره میکند و با استفاده از این فایل میتوان نام میزبان را تغیر داد.

- [ ] Write your description about /proc/self file
    - [ ] `[FILL HERE with your description]`
    - [ ] این شاخه مربوط به پروسه جاری است و به برنامه نویسان این امکان را میدهد که با استفاده از این، راحت تر به اطلاعات مختلف پروسه فعلی دسترسی داشته باشند.
     
    - [ ] **`/proc/self/exe`**:
          این فایل نشاندهنده مسیر فایل اجرایی برنامه جاری است.

    - [ ] **`/proc/self/fd`**:
          این دایرکتوری همه فایل های باز را برای پروسه جاری نشان میدهد.
    - [ ] **`/proc/self/status`**:
          این فایل خاوی اطلاعات متوعی است درباره وضعیت پروسه جاری مثل حافظه که پروسه جاری استفاده میکند.


## Source Code Submission

please submit all your codes in a zip file

 - [ ] `Zip File HERE`
