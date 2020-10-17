# Operating-System--pthreads
Program writing in C/C++ simulating the enforcement of these restrictions using use of pthreads, pthread mutexes and pthread condition variables.

### SPECIFICATION
This project will familiarize you with the use of pthreads, pthread mutexes and pthread condition variables.

### PROBLEM:
A car tunnel is so poorly ventilated that it has become necessary to restrict:
```
1. The number of northbound cars in the tunnel,
2. The number of southbound cars in the tunnel,
3. The total number of cars in the tunnel.
```
Your assignment is to write a C/C++ simulating the enforcement of these restrictions using Pthread mutexes and condition variables.    
Your program should consist of    
1. A main thread that will fork a tunnel process and the car processes according to the input specifications.   
2. One car thread per car wanting to cross the tunnel. The input to your program consists of the maximum number of northbound cars in the tunnel, the maximum number of southbound cars , and the maximum total number of cars in the tunnel followed by an ordered list of arriving cars as in:
```
3 // up to three cars at a time
2 //up to two NB cars at a time
2 //up to two SB cars at a time
1 S 3 // SB car arrives at t = 1s
// will take 3s to go through the tunnel
2 N 4 // northbound car arrives 2s after
// will take 4s to go through the tunnel
1 S 4 // southbound car arrives 1s after
// will take 4s to go through the tunnel
```
Your program will terminate when all cars have gone through the tunnel.

### OUTPUT
Your program should start by echoing the first here lines
of input as in:
Maximum number of cars in the tunnel: 2
Maximum number of northbound cars: 1
Maximum number of southbound cars: 1
It should print one line of output each time a car (a)
arrives at the tunnel, (b) enters the tunnel and (c) leaves
the tunnel. This line of output should identify each car
by its northbound or southbound sequence number as in
Southbound car # 1 arrives at the tunnel.
Southbound car # 1 enters the tunnel.
Northbound car # 1 arrives at the tunnel.
Northbound car # 1 enters the tunnel.
Southbound car # 2 arrives at the tunnel.
Northbound car # 2 arrives at the tunnel.
Southbound car # 1 exits the tunnel.
Southbound car # 2 enters the tunnel.
At the end of the simulation, your program should also
print a summary with the total number of northbound
and southbound cars that went through the tunnel as well
as the total number of cars that had to wait because of
the restrictions.
This summary could look like:
2 northbound car(s) crossed the tunnel.
2 southbound car(s) crossed the tunnel.
2 car(s) had to wait.

