# Virtual-Memory-Manager

Team Members: Rudy Leiva, Daniel Hernandez

How to compile and run:

Linux/UNIx & Mac OS X: Open terminal, cd to the directory where the source file is stored.
Run "gcc -o VirtualMem VirtualMem_Manager.c" on the terminal window. To run the program, type "./VirtualMem addresses.txt"

Windows 7/8/10: Use IDE software "Code Blocks" to compile and run this program.

Files included:

VirtualMem_Manager.c //source code
VirtualMem           //c executable file
addresses.txt        //file containing 1000 addresses
BACKING_STORE.bin    //binary file

Description of program:

The purpose of Project 5 was for the students to learn how to convert a logical address to a physical address by instantiating and
using our own page table and tlb. The program verifies that a valid text file has been input in the command prompt when running the program
Next, the program opens 2 files for reading, addresses.txt and BACKING_STORE.bin and creates another file for writing, Output.txt. The program
will print its outputs into this file, but it will not print the outputs on the command prompt since not all of the outputs are displayed. 
Then the program will continue with the reading of each address and get the page number and offset number for each address. Then it consults
the tlb to see if the page number is already in the tlb. if it is, then it is a tlb hit and proceeds to get the frame number and the physical page number.
Then it stores the values of the offset and the physical page number in a variable, giving us the physical address. If it is not in the tlb,
then it will be a tlb miss and will go to the page table to get the physical address number from the page table. If it goes to the page table it is a page fault.
then it will store the physical address and the offset in a variable which would give us the physical address.

*******************************************************************NOTE************************************************************************************************
The program will not print its output on the command prompt but instead will print its output in a text file called "Output.txt".
************************************************************************************************************************************************************************

Team member contributions:

Rudy Leiva:
Research on TLB
FIFO algorithm
Structures in c
opening and reading the bin file in c
README file
coding
debugging

Daniel Hernandez:
Research on Page Table
fseek()
fread()
memset()
page number and offset number
codding 
debugging
