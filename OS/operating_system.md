- Operating system is the lowest layer of software that sits over the hardware.
- Operating system exposes interface through which application can run on stop of it. 
***

## Introduction to UNIX system call PART 1
 - In inital days UNIX shell provides following functionalities:
    1. Start or Load a new program.
    2. Open, Read, or Write files.
    3. Exit 
- Intially shell was part of OS, but in modern OS shell run as separate application, thus OS should provide all functioanlities mentiond above to application's.
- These functionalities of OS are kernel functions also known as '**System Calls**'. 

(Continuing with the model where shell was not part of OS)
- UNIX provide `fork()` and `exec()` system call to start a program.
- ### `exec()` system call:
    1. This system call takes file name as parameter, i.e `exec(<file name>)`.
    2. It searches for file in the pwd and loads the file, replacing the shell.
    3. Since shell itself was running as application, there is no way to return the control to the shell again.
    4. This was not the problem with model where shell was part of OS.
- ### `fork()` system call:
    1. Similar to `exec()`, fork also takes file name as a parameter.
    2. What makes it different, is that when `fork()` call is made first `fork()` create a copy of current process (**child process**) with same state(program counter).
    3. Now child process makes the `exec()` system call with same file name as in passed to `fork()` intially.
    4. Since parent and child process are exact replica, how to differentiate b/w them? `fork()` call returns a value **pid**. For **parent** process return value be the **pid of child process**, and for **child** process `fork()` return value will any **value that cannot be pid i.e 0(zero)**.
- All the access to the hardware resources was mediate by OS, to different applications.
- One contributiion of UNIX was introduction to general interface for mediating allocation to variety of resources, that interface is:
    1. `open()`
    2. `read()`
    3. `write()`
    4. `close()`
    - Generally if resource get allocated following calls return positive values else negative value.
    ```c++
    fd = open(<file name>);
    ret = read(fd, buf, 100);
    ret = write(d, buf, 100);
    close(fd);
    ```
- Each process has its own file descriptor table.
    <table>
        <tr>
            <th>Desciptor number</th>
            <th> Resource</th>
        </tr>
        <tr>
            <td>0: STDIN</td>
            <td>Keyboard</td>
        </tr>
        <tr>
            <td>1: STDOUT</td>
            <td>Console</td>
        </tr>
        <tr>
            <td>2: STDERR</td>
            <td>Console</td>
        </tr>
        <tr>
            <td>3</td>
            <td></td>
        </tr>
        <tr>
            <td>4</td>
            <td></td>
        </tr>
    </table>
- This file descriptor program is kept hidden from the program, but progarm can manipulate the table by the `open / close` calls.
- Each process has its three special file descriptor 0, 1, 2, the idea is a program will read from its standard input, will write to its standard output, and if some error occurs the standard error.
- Operating system is responsible for deciding what is the stdin, stdout, and stderr for an program.
***

## Introduction to UNIX system call PART 2
- Sample Shell Program
    ```c++
    while(1)
    {
        write(1, "$", 2);
        readcommand(0, commands, args);
        
        if((pid = fork()) == 0)
        exec(command, args);
        
        else if(pid > 0)
        wait();
        
        else
        printf("Error in fork");     
    }
    ```
***
