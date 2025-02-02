- [learnpdc](https://www.learnpdc.org/)
   - [CSinParallel](https://csinparallel.org/index.html)
   - [Raspberry Pi Handout](https://www.learnpdc.org/RaspberryPiHandout/index.html)
   - [Distributed Computing Using MPI and the Raspberry Pi](https://www.learnpdc.org/RaspberryPi-mpi/)

- [What are the differences between MPI and OpenMP? (StackSE)](https://stackoverflow.com/questions/32464084/what-are-the-differences-between-mpi-and-openmp)
- [openMP vs openMPI (NMUni)](https://hpc.nmsu.edu/discovery/mpi/mpi-openmp/#:~:text=A%20thread%2Dbased%20parallelism.,passing%20messages%20to%20each%20other.)
- [Introduction to Parallel Programming with MPI](https://rantahar.github.io/introduction-to-mpi/index.html)
- [INTERMEDIATE MPI](https://enccs.github.io/intermediate-mpi/)
```
lscpu
top      # press 1
time -p executable [arguments]
```

# openMP
```
#include <math.h>
#include <stdio.h> // printf()
#include <stdlib.h> // atoi()
#include <omp.h> // OpenMP

int main(int argc, char** argv)
{
   int array[SIZE];

   if (argc > 1)
   {
        omp_set_num_threads( atoi(argv[1]) );
   }


#ifdef _OPENMP
    omp_set_num_threads( threadcnt );
    printf("OMP defined, threadct = %d\n", threadcnt);
#else
    printf("OMP not defined");
#endif


   return 0;
}
```


```
 #pragma omp parallel
 {
     int id = omp_get_thread_num();
     int numThreads = omp_get_num_threads();
 }

// choose one!
#pragma omp parallel for
#pragma omp parallel for schedule(static,1)
#pragma omp parallel for schedule(dynamic,1)
 for (int i = 0; i < REPS; i++)
{
}



#pragma omp parallel for \
private(i) shared (a, n, h, integral) reduction(+: integral)
for(i = 1; i < n; i++)
{
   integral += i
}

```



race conditions and the reduction clause
