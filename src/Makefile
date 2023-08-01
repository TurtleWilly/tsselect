
CC = gcc
CFLAGS = -O2 -D_XOPEN_SOURCE=600 -D_FILE_OFFSET_BITS=64
LDFLAGS =
OBJS = tsselect.o
PROGRAM = tsselect
PREFIX = /usr/local
DEST = $(PREFIX)/bin

$(PROGRAM): $(OBJS)
	$(CC) $(LDFLAGS) -o $@ $(OBJS)

.c.o:
	$(CC) $(CFLAGS) -c $<

all:$(PROGRAM)

clean:
	rm $(OBJS) $(PROGRAM)

install:$(PROGRAM)
	mkdir -p $(DEST)
	install -s $(PROGRAM) $(DEST)
