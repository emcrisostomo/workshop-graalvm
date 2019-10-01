all: gzip.bc

gzip.bc: gzip.c
	clang -c -O1 -emit-llvm gzip.c
