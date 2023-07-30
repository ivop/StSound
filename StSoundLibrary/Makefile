
CXX ?= g++

OBJS = LZH/LzhLib.o digidrum.o Ymload.o Ym2149Ex.o YmMusic.o YmUserInterface.o
CXXFLAGS = -O2

all: libstsound.a

libstsound.a: $(OBJS)
	ar cr libstsound.a $(OBJS)

clean:
	rm -f *~ *.o *.a */*.o */*~
