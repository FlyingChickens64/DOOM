##########################################################
#
# $Id:$
#
# $Log:$
#
#

CC=gcc
CFLAGS=-m32 -O -DNORMALUNIX -DLINUX
LDFLAGS=-L/usr/lib/i386-linux-gnu
LIBS=-lm

O=linux

all:	 $(O)/sndserver
$(shell mkdir -p $(O))

clean:
	rm -f *.o *~ *.flc
	rm -f linux/*

# Target
$(O)/sndserver: \
	$(O)/soundsrv.o \
	$(O)/sounds.o \
	$(O)/wadread.o \
	$(O)/linux.o
	$(CC) $(CFLAGS) $(LDFLAGS) \
	$(O)/soundsrv.o \
	$(O)/sounds.o \
	$(O)/wadread.o \
	$(O)/linux.o -o $(O)/sndserver $(LIBS)
	echo make complete.

# Rule
$(O)/%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@


