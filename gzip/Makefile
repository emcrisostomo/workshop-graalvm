all: gzip.bc

run: gzip.bc testfile.gz
	-rm testfile
	lli gzip.bc -d testfile.gz

testfile.gz:
	cp war-and-peace.txt.gz $@

gzip.bc: gzip.c
	clang -c -O1 -emit-llvm gzip.c
