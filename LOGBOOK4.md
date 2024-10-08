# Trabalho realizado na Semana #4 

## Task 1
![Fig 1_1](./imgs/LOGBOOK4/task1_1.png)

![Fig 1_2](./imgs/LOGBOOK4/task1_2.png)

![Fig 1_3](./imgs/LOGBOOK4/task1_3.png)

![Fig 1_4](./imgs/LOGBOOK4/task1_4.png)

## Task 2
- Step 1:

![Fig 2_1](./imgs/LOGBOOK4/task2_1.png)

_Program_

![Fig 2_2](./imgs/LOGBOOK4/task2_2.png)

![Fig 2_3](./imgs/LOGBOOK4/task2_3.png)

- Step 2:

![Fig 2_4](./imgs/LOGBOOK4/task2_4.png)

_Changed program_

![Fig 2_5](./imgs/LOGBOOK4/task2_5.png)

![Fig 2_6](./imgs/LOGBOOK4/task2_6.png)

![Fig 2_7](./imgs/LOGBOOK4/task2_7.png)

_Conclusion:_ When a fork() is made in a program, the child and the parent process have the same environment, so there’s no difference between them.

## Task 3
- Step 1:

![Fig 3_1](./imgs/LOGBOOK4/task3_1.png)

_Program_

![Fig 3_2](./imgs/LOGBOOK4/task3_2.png)

- Step 2:

![Fig 3_3](./imgs/LOGBOOK4/task3_3.png)

![Fig 3_4](./imgs/LOGBOOK4/task3_4.png)

_Conclusion:_  
* If you pass `NULL` as the third argument to `execve`, the new program starts with an empty environment. 
* If you pass `environ` as the third argument to `execve`, the new program inherits the environment variables from the calling program.


## Task 4

![Fig 4_1](./imgs/LOGBOOK4/task4_1.png)

_Program_

![Fig 4_2](./imgs/LOGBOOK4/task4_2.png)

_Conclusion:_ Both execve() and system() prints on shell the environmental variables, although they don´t work the same way.
* System() creates “automatically the child process that allows it to execute the shell command.
* Execve() replaces the current process with the request command.



## Task 5
- Step 1:

![Fig 5_1](./imgs/LOGBOOK4/task5_1.png)

_Program_

- Step 2:
![Fig 5_2](./imgs/LOGBOOK4/task5_2.png)

- Step 3:
![Fig 5_3](./imgs/LOGBOOK4/task5_3.png)

_Conlusion:_ When we run the child process the environment variable LD_LIBRARY_PATH doesn´t appear, which was a surprise


## Task 6
In the context of a SET-UID program, which runs with the owner's privileges, a user can manipulate the program's Environment Variables (EVs) to their advantage. In the given scenario, there's a program that executes the 'ls' command by invoking the 'system' function. The goal is to trick this program into calling an altered version of 'ls' with higher privileges.

However, there's a challenge: when 'system' is called, it ultimately leads to the execution of '/bin/dash,' a shell that has built-in safeguards. These safeguards reduce the process's permissions to match the user's privileges. To work around this, we need to change the shell program to something else, like '/bin/zsh.'

To facilitate this exploitation, the following steps were taken:

1. The PATH environment variable was extended to include '/home/seed,' giving the system access to this directory.

2. An alternative version of 'ls' was created in the '/home/seed' directory. This custom 'ls' performed an action that's typically restricted to root.

3. The program was then compiled and configured as a SET-UID program, which means it runs with elevated privileges.
