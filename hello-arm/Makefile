CFLAGS := -c -Wall -I../inc
PROGS := hello-arm-static hello-arm-shared

all: $(PROGS)

hello-arm.o: hello-arm.c
	arm-cortex_a8-linux-gnueabihf-cc $(CFLAGS) -o $@ $^

hello-arm-static: hello-arm.o
#	$(CC) $(LDFLAGS) -o $@ $^ ../static/libtest.a
	arm-cortex_a8-linux-gnueabihf-cc -o $@ $^ -L../static -ltest

hello-arm-shared: hello-arm.o
	arm-cortex_a8-linux-gnueabihf-cc -o $@ $^ -L../shared -ltest

clean:
	rm -f *.o
	rm -f $(PROGS)

install:
	cp $(PROGS) $(TARGET_DIR)/usr/local/bin
