# Makefile for lib/i86/misc.

CFLAGS	= -O -D_MINIX -D_POSIX_SOURCE -Was-ncc
CC1	= $(CC) $(CFLAGS) -c

LIBRARY	= ../../libc.a
all:	$(LIBRARY)

OBJECTS	= \
	$(LIBRARY)(alloca.o) \
	$(LIBRARY)(getprocessor.o) \
	$(LIBRARY)(iolib.o) \

$(LIBRARY):	$(OBJECTS)
	aal cr $@ *.o
	rm *.o

$(LIBRARY)(alloca.o):	alloca.s
	$(CC1) alloca.s

$(LIBRARY)(getprocessor.o):	getprocessor.s
	$(CC1) getprocessor.s

$(LIBRARY)(iolib.o):	iolib.s
	$(CC1) iolib.s
