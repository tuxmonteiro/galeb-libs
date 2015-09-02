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

test:
	gcc -c Core_test.cpp
	gcc -W1 -lc++ -lboost_unit_test_framework -o Core_test.out Core_test.o
	echo
	./Core_test.out

.PHONY: clean test dynamic shared

clean:
	rm -rf *.o *.so *.dylib *.out ../lib/*
