CFLAGS := -Wall -g -fPIC -I../inc
OBJECTS := testlib.o
 
all: libtest.so

# Build the shared library
libtest.so: $(OBJECTS)
	arm-cortex_a8-linux-gnueabihf-cc -shared -o libtest.so $(OBJECTS)

testlib.o: testlib.c
	arm-cortex_a8-linux-gnueabihf-cc $(CFLAGS) -c testlib.c
clean:
	rm -f $(OBJECTS)
	rm -f libtest.so
