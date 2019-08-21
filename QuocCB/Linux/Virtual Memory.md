Virtual memory was developed at a time when physical memory -- the installed RAM -- was expensive. Computers have a finite amount of RAM, so memory can run out, especially when multiple programs run at the same time. A system using virtual memory uses a section of the hard drive to emulate RAM. With virtual memory, a system can load larger programs or multiple programs running at the same time, allowing each one to operate as if it has infinite memory and without having to purchase more RAM.

While copying virtual memory into physical memory, the OS divides memory into pagefiles or swap files with a fixed number of addresses. Each page is stored on a disk and when the page is needed, the OS copies it from the disk to main memory and translates the virtual addresses into real addresses.

### History
Before virtual memory was developed, computers had RAM and secondary memory. Early computers used magnetic core memory for main memory and magnetic drums for their secondary memory. Computer memory was expensive and usually in short supply back in the 1940s and 1950s. As computer programs grew in size and complexity, developers had to worry that their programs would use up all of a computer's main memory and run out of memory.

In those early days, programmers used a process called overlaying to run programs that were larger than available memory. Parts of a program that weren't continually in use were set up as overlays that, when needed, would overwrite the existing overlay in memory. It required extensive programming to make overlaying work, and that was a key impetus for the development of automated virtual memory.

German physicist Fritz-Rudolf Güntsch is credited with developing the concept of virtual memory in 1956 as part of his doctoral work. In it he described a computer that used hardware to automatically move blocks of data between primary and secondary memory to avoid running out of main memory. This formed the basis for paging, a process in which memory is divided into sections and transferred between RAM and a hard drive to free up space in RAM. Paging began to show up in commercial computers in the early 1960s.

In 1969, IBM researchers demonstrated that what was by then called a virtual memory overlay system worked better than the earlier manual systems. Mainframes and minicomputers in the 1970s generally used virtual memory. Virtual memory technology was not included in early personal computers because developers thought running out of memory would not be a problem in those machines. That assumption proved incorrect. Intel introduced virtual memory in the protected mode of the 80286 processor in 1982 and paging support when the 80386 came out in 1985.

### Types of virtual memory
A computer's memory management unit (MMU) handles memory operations, including managing virtual memory. In most computers, the MMU hardware is integrated into the CPU. There are two ways in which virtual memory is handled: paged and segmented.

Paging divides memory into sections or paging files, usually approximately 4 KB in size. When a computer uses up its RAM, pages not in use are transferred to the section of the hard drive designated for virtual memory using a swap file. A swap file is a space set aside on the hard drive as the virtual memory extensions of the computer's RAM. When the swap file is needed, it's sent back to RAM using a process called page swapping. This system ensures that computer's OS and applications don't run out of real memory.

 
This video discusses paging without virtual memory.
The paging process includes the use of page tables, which translate the virtual addresses that the OS and applications use into the physical addresses that the MMU uses. Entries in the page table indicate whether or not the page is in real memory. If the OS or a program doesn't find what it needs in RAM, then the MMU responds to the missing memory reference with a page fault exception to get the OS to move the page back to memory when it's needed. Once the page is in RAM, its virtual address appears in the page table.

Segmentation is also used to manage virtual memory. This approach divides virtual memory into segments of different lengths. Segments not in use in memory can be moved to virtual memory space on the hard drive. Segmented information or processes are tracked in a segment table, which shows if a segment is present in memory, whether it's been modified and what its physical address is.

 
Jacob Schrum reviews the use of virtual memory
with segmentation.
Some virtual memory systems combine segmentation and paging. In this case, memory gets divided into frames or pages. The segments take up multiple pages and the virtual address includes both the segment number and the page number.

### How to manage it
Operating systems have default settings that determine the amount of hard drive space to allocate for virtual memory. That setting will work for most applications and processes, but there may be times when it's necessary to manually reset the amount of hard drive space allocated to virtual memory, such as with applications that depend on fast response times or when the computer has multiple HDDs.

When manually resetting virtual memory, the minimum and maximum amount of hard drive space to be used for virtual memory must be specified. Allocating too little HDD space for virtual memory can result in a computer running out of RAM. If a system continually needs more virtual memory space, it may be wise to consider adding RAM.

### Pros of using virtual memory
Among the primary benefits of virtual memory is its ability to handle twice as many addresses as main memory. It uses software to consume more memory by using the HDD as temporary storage while MMUs translate virtual memory addresses to physical addresses via the CPU. Programs use virtual addresses to store instructions and data; when a program is executed, the virtual addresses are converted into actual memory addresses.

Virtual memory and memory hierarchy
Virtual memory also frees applications from managing shared memory and saves users from having to add memory modules when RAM space runs out.

### Limitations
 
Mike Murphy explains virtual memory in this
video tutorial.
The use of virtual memory has its tradeoffs, particularly with speed. It's generally better to have as much physical memory as possible so programs work directly from RAM or physical memory. The use of virtual memory slows a computer because data must be mapped between virtual and physical memory, which requires extra hardware support for address translations.


In a virtualized computing environment, administrators can use virtual memory management techniques to allocate additional memory to a virtual machine (VM) that has run out of resources. Such virtualization management tactics can improve VM performance and management flexibility.

