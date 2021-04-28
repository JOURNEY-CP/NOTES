# Process Data Structures and Satte Transictions
## Process Management
A process is basically a program in execution. The execution of a process must progress in a sequential fashion.

A Program/Process here Refers any code
```cpp
// Example code
#include<iostream>
int main(){
  int a,b;
  cin>>a>>b;
  cout<<a+b<<endl;
}
```
Memory of every process is broadly devided into 4 types
1. **Stack** : Where all temporary data such as method/function parameters, return address and local variables etc will be present.
2. **Heap** :  temporary data such as method/function parameters, return address and local variables.
3. **Text** : Other core data like program counter and data of registers involved
4. **Data**: Globl and static variables 

## Process table
The process table is a data structure maintained by the operating system to facilitate context switching and scheduling, and other activities

- Each Process is alloted by a unique identification number (PID)
- This is connected to PCB to have a control over all processes
- Here the process means any task. My be a small c++ code which adds 2 numbers
## PCB (Process Control Block)
- PCB stores all the meta details related to project.
- Meta details include 
  - **process state**: The current state of the process (you can think of a c++ sum of two numbers code whch is stopped after scanning. Now so much data is stored so that if we go to another process and comes back here we can continue)
  - **pointer**: A stack pointer required to remember when we are going to other process
  - Process Number: PID
  - **Program Counter (PC)**: stores the address of next instruction which needs to run
  - **Memory Limits**: All memory occupied for the process
  - **Open FIles list**: Files opened for the purpose of process 
![![picture 2](images/pic_1619606163740.png)  1](images/pic_1619606193330.png)  

- Here Process table stroes pid and pcb pointer
- PCB stores all the meta data reg process
- As all the current systems are multi processing enables these 2 parts are needed.
## PTE (Process Table Entry)
- Each entry to the process table is called process table entry
## Process States
![picture 4](images/pic_1619606617432.png)  
- **New**: Process is taken into consideration
- **Ready**: Process is ready to run
- **Run**: Running
- **Wait/Block**: waiting as another process is runnning ot Blocked (may be this is dependent on other processes). Genrally occur when dependent on Input Output (IO)
- **Suspend Wait**: Waiting for IO
- **Suspend Ready**: Ready after IO
- All ths data will be stored in PCB which is linked in Process Table
## Transition Diagram
The Transactions which are used in between Process States

Ex: The IO event Wait and copmletion are two transitions

some people may also represent transitions like this
![picture 5](images/pic_1619629137103.png)  

## Context of Process Levels
### User Level
### kernel Level
### Process Level