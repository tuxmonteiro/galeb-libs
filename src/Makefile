LIBNAME=undef

all:

dynamic:
	gcc -c -fPIC $(LIBNAME).c
	gcc -dynamiclib -lncurses -r/usr/lib -o lib$(LIBNAME).dylib XXX.o
	cp -f lib$(LIBNAME).dylib ../lib/libXXX.dylib

shared:
	gcc -c -fPIC $(LIBNAME).c
	gcc -shared -W1 -lncurses -r/usr/lib -soname,lib$(LIBNAME).so -o libXXX.so XXX.o
	cp lib$(LIBNAME).so ../lib/libXXX.so

.PHONY: clean

clean:
	rm -rf *.o *.so *.dylib ../lib/*
