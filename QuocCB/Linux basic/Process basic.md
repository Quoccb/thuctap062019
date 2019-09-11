A process refers to a program in execution; it’s a running instance of a program. It is made up of the program instruction, data read from files, other programs or input from a system user.

#### Types of Processes

There are fundamentally two types of processes in Linux:

- **Foreground processes** (also referred to as interactive processes) – these are initialized and controlled through a terminal session. In other words, there has to be a user connected to the system to start such processes; they haven’t started automatically as part of the system functions/services.
- **Background processes** (also referred to as non-interactive/automatic processes) – are processes not connected to a terminal; they don’t expect any user input.

#### What is Daemons

These are special types of background processes that start at system startup and keep running forever as a service; they don’t die. They are started as system tasks (run as services), spontaneously. However, they can be controlled by a user via the init process.

#### Creation of a Processes in Linux

A new process is normally created when an existing process makes an exact copy of itself in memory. The child process will have the same environment as its parent, but only the process ID number is different.

There are two conventional ways used for creating a new process in Linux:

- **Using The System() Function** – this method is relatively simple, however, it’s inefficient and has significantly certain security risks.
- **Using fork() and exec() Function** – this technique is a little advanced but offers greater flexibility, speed, together with security.

#### How Does Linux Identify Processes?
Because Linux is a multi-user system, meaning different users can be running various programs on the system, each running instance of a program must be identified uniquely by the kernel.

And a program is identified by its process ID (PID) as well as it’s parent processes ID (PPID), therefore processes can further be categorized into:

- **Parent processes** – these are processes that create other processes during run-time.
- **Child processes** – these processes are created by other processes during run-time.

#### The init Process

Init process is the mother (parent) of all processes on the system, it’s the first program that is executed when the Linux system boots up; it manages all other processes on the system. It is started by the kernel itself, so in principle it does not have a parent process.
<br>The init process always has process ID of 1. It functions as an adoptive parent for all orphaned processes.
<br>You can use the pidof command to find the ID of a process.

#### Starting a Process in Linux
Once you run a command or program (for example cloudcmd – CloudCommander), it will start a process in the system. You can start a foreground (interactive) process as follows, it will be connected to the terminal and a user can send input it:

#### States of a Process in Linux
During execution, a process changes from one state to another depending on its environment/circumstances. In Linux, a process has the following possible states:

- **Running** – here it’s either running (it is the current process in the system) or it’s ready to run (it’s waiting to be assigned to one of the CPUs).
- **Waiting** – in this state, a process is waiting for an event to occur or for a system resource. Additionally, the kernel also differentiates between two types of waiting processes; interruptible waiting processes – can be interrupted by signals and uninterruptible waiting processes – are waiting directly on hardware conditions and cannot be interrupted by any event/signal.
- **Stopped** – in this state, a process has been stopped, usually by receiving a signal. For instance, a process that is being debugged.
- **Zombie** – here, a process is dead, it has been halted but it’s still has an entry in the process table.