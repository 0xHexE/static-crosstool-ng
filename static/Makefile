CFLAGS = -Wall -g -I../inc
OBJECTS = testlib.o
 
all: libtest.a

# Build the static library
libtest.a: $(OBJECTS)
	ar rc libtest.a $(OBJECTS)

testlib.o: testlib.c
	arm-cortex_a8-linux-gnueabihf-cc $(CFLAGS) -c testlib.c

clean:
	rm -f $(OBJECTS)
	rm -f libtest.a
