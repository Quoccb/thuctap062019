
**1. The kernel.**

The kernel is the heart of the system. It manages the communication between the underlying hardware and the
peripherals. The kernel also makes sure that processes and daemons (server processes) are started and stopped
at the exact right times. The kernel has a lot of other important tasks, so many that there is a special
kernel-development mailing list on this subject only, where huge amounts of information are shared. It would
lead us too far to discuss the kernel in detail. For now it suffices to know that the kernel is the most important file on the system.

**Four broad categories of kernels:**

- **Monolithic** kernels provide rich and powerful abstractions of the underlying hardware.<br>
- **Microkernels** provide a small set of simple hardware abstractions and use applications called servers to provide more functionality.<br>
- **Exokernels** provide minimal abstractions, allowing low-level hardware access. In exokernel systems, library operating systems provide the<br>- **abstractions** typically present in monolithic kernels.<br>
- **Hybrid (modified microkernels)** are much like pure microkernels, except that they include some additional code in kernelspace to increase performance.

**2. Linux Architechture.**

<img src=https://2.bp.blogspot.com/-xU5aB5e7v9E/WfAvTqZbDkI/AAAAAAAAJAo/-0s8WE4OOyE1_YZDjFLhGc4IWQ8IONEXwCLcBGAs/s1600/ksa-pic0.jpeg>

- **The shell** is an interface between the user and the kernel, and it affords services of the kernel.
It takes commands from the user and executes kernel’s functions. 
The Shell is present in different types of operating systems, which are classified into two types:
    - command line shells 
    - graphical shells.
 
    The command line shells provide a command line interface, while the graphical line shells provide a graphical user interface. Though both shells perform operations, but the graphical user interface shells perform slower than the command line interface shells. Types of shells are classified into four:

    - Korn shell
    - Bourne shell
    - C shell
    - POSIX shell
