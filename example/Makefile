CC=gcc
CFLAGS=-g -I../src/include -g -O2
LIBNDPI=../src/lib/libndpi.a
LDFLAGS=$(LIBNDPI) -lpcap -lpthread 
OBJS=ndpiReader.o ndpi_util.o

all: ndpiReader

ndpiReader: $(OBJS) $(LIBNDPI)
	$(CXX) $(CFLAGS) $(OBJS) -o $@ $(LDFLAGS)

%.o: %.c $(HEADERS) Makefile
	$(CC) $(CFLAGS) -c $< -o $@

install:
	cp ndpiReader /usr/local/bin

clean:
	/bin/rm -f *.o ndpiReader

