# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to a repository to complete the task. Remember to also submit your answers to Blackboard

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is when multiple tasks or processes run after each other. It manages to make theese tasks seem concurrent by switching between theese tasks fast. This procedure is called scheduling.

 > Paralellism is when you run many processes at the same time by runnning them on different cores or processors. This enebles the computers to do much more than if only one concurrent process can run at a time.

 ### Why have machines become increasingly multicore in the past decade?
 > Machines have bocome more multicore the past decade because it is impossible to encrese the performace of processors enough by only encrese clock frequency, since this produces to much heat. To overcome this limitation, we design computers that deployes more than one core at a time. This is called multiprocessor computers

 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Concurrent programming help solve problems where you have to do multiple things at the same time. This can be listening to a IP-socket while processing data eg.

 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > It makes the life of the programmer much harder. This is because it introduces problems that doesn't exsist when you only have one concurrent thread. These problems often arrise when different part of the program need to access the same piece of data.

 ### What are the differences between processes, threads, green threads, and coroutines?
 >  A processes (at Least in Linux) is a complete program with and data, code and state which can be scheduled. Threads can be regarded as lightweight processes in the sense that they often lack some of features that processes have. How threads work are dependent on the OS. In Linux real threads doesn't exist, as they do in Windows. You can stil have soft threads (also called green threads), but theese are defined inside each programming language, and are not part of the OS. Coroutines are almost the same as threads, only that they are not scheduled preemptive. This allowes for concurrency but not paralellism.

 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > They make green threads.

 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > The GIL makes it impossible for python programms to run more than one process.

 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > THe solution to this is to use the Multiprocessing library in python.

 ### What does `func GOMAXPROCS(n int) int` change?
 > This limits the number of OS level processes that the program can spawn.
