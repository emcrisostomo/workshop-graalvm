all: gzip.bc
run:
	lli gzip.bc $(ARGS)

gzip.bc: gzip.c
	clang -c -O1 -emit-llvm gzip.c
