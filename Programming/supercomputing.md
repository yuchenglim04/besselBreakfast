- [learnpdc](https://www.learnpdc.org/)
- [CSinParallel](https://csinparallel.org/index.html)
- [Raspberry Pi Handout](https://www.learnpdc.org/RaspberryPiHandout/index.html)


- [What are the differences between MPI and OpenMP?](https://stackoverflow.com/questions/32464084/what-are-the-differences-between-mpi-and-openmp)
- [Introduction to Parallel Programming with MPI](https://rantahar.github.io/introduction-to-mpi/index.html)
- [INTERMEDIATE MPI](https://enccs.github.io/intermediate-mpi/)
```
lscpu
top      # press 1

```

# openMP
```
#include <omp.h>     // OpenMP

int main(int argc, char** argv) {
   int array[SIZE];

   if (argc > 1) {
        omp_set_num_threads( atoi(argv[1]) );
   }

```
