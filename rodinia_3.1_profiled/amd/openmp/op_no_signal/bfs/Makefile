# C compiler
CC = g++
ICC = icc
CC_FLAGS = -g -fopenmp -O0

all: bfs bfs_offload

bfs: bfs.cpp 
	$(CC) $(CC_FLAGS) cpu_check.c bfs.cpp -o bfs 

bfs_offload: bfs.cpp
	$(ICC) $(CC_FLAGS) -DOMP_OFFLOAD bfs.cpp -o bfs_offload

clean:
	rm -f bfs bfs_offload result.txt
