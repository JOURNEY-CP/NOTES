# Process Control
## Process Creation
A Process is created in many ways which include
- **Creation by User**: when we open a app/code 
- **System Initialization**: Some processes may be initialized by sytem or kernal directly. Many processes will automatically start at starting of system.
- **BatchJobs**: Processes which run as sheduled. (no further user interaction needed)
- **By Running Process**: A process may be created by some other process
## Process Termination
A Process can be terminated in many ways which include
- Naturally completed: End of program
- Intrupt by user: probablly with signals
- Any Failure
- Memory scarcity: If process needs much memory
- Need of Other Resource: If a process requests to access resourses other than alloted it will be killed (Ex: Segmentation fault)
- Parent Process: May be terminated by parent process or sometimes if parent process is killed all child processes will be killed 
## Parent and Child Processes
When a process $A$ creates a process $B$ then process $A$ is called Parent process and process $B$ is called child process.
## System Calls
### fork()

### exit()

### wait()

### kill()

## Signal Handling

## Process Sheduling Stratagies
### FCFS

### SPN

### SRT

### Round Robin

### HRRN

### Fair Share Sheduling
