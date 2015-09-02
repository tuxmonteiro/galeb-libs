LIBNAME=galeb

all:

dynamic:
	gcc -c -fPIC $(LIBNAME).cpp
	gcc -dynamiclib -lc++ -o lib$(LIBNAME).dylib $(LIBNAME).o
	cp -f lib$(LIBNAME).dylib ../lib/lib$(LIBNAME).dylib

shared:
	gcc -c -fPIC $(LIBNAME).cpp
	gcc -shared -W1 -lc++ -o lib$(LIBNAME).so $(LIBNAME).o
	cp lib$(LIBNAME).so ../lib/lib$(LIBNAME).so

.PHONY: clean

clean:
	rm -rf *.o *.so *.dylib ../lib/*
