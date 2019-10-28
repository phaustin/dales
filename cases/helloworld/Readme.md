# compiling and running helloworld.f90 on optimum

1. cd dales/cases/helloworld
1. mkdir build
1. cd build
1. cmake ..
1. make install

This should build helloworld.f90 and copy it into ~/bin

Next, reserve a node to run this on interactively:

To do this, use the command

Iqsub hours nodes processors_per_node to get 30 minutes
on 1 node with 20 processors

```
Iqsub 0.5 1 20
```

and to run it on 20 processors and see the output:

mpiexec -n 20 ~/bin/helloworld

which should print out something like:

```
(work) [paustin@n037 build]$ mpiexec -n 20 ~/bin/helloworld
mpiexec -n 20 ~/bin/helloworld
Hello, World! I am process  1 of 20 on n037.
Hello, World! I am process  2 of 20 on n037.
Hello, World! I am process  3 of 20 on n037.
Hello, World! I am process  4 of 20 on n037.
Hello, World! I am process  5 of 20 on n037.
Hello, World! I am process  7 of 20 on n037.
Hello, World! I am process  9 of 20 on n037.
Hello, World! I am process 10 of 20 on n037.
Hello, World! I am process 11 of 20 on n037.
Hello, World! I am process 13 of 20 on n037.
Hello, World! I am process 14 of 20 on n037.
Hello, World! I am process 16 of 20 on n037.
Hello, World! I am process 17 of 20 on n037.
Hello, World! I am process 18 of 20 on n037.
Hello, World! I am process 19 of 20 on n037.
Hello, World! I am process  8 of 20 on n037.
Hello, World! I am process 15 of 20 on n037.
Hello, World! I am process  0 of 20 on n037.
Hello, World! I am process  6 of 20 on n037.
Hello, World! I am process 12 of 20 on n037.
```

# when you're done, type

```
exit
```

to return the node to the pool.




