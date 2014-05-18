IDIR=../include 
CC=gcc 
CFLAGS=-I$(IDIR) 
EXEC=hellomake 

LDIR=../lib 

LIBS=-lm 

_DEPS=hellomake.h 
DEPS=$(patsubst %, $(IDIR)/%, $(_DEPS)) 

OBJ=hellomake.o hellofun.o 

%.o: %.c $(DEPS) 
	$(CC) -c -o $@ $< $(CFLAGS) 

$(EXEC): $(OBJ) 
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS) 

.PHONY: clean distclean 

clean: 
	rm -rf *.o *~ core $(INCDIR)/*~ 

distclean: 
	make clean 
	rm -rf $(EXEC) 


