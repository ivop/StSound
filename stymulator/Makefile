CXX ?= g++

all: ymplayer

PLAYEROBJS = sound.o ui.o ymplayer.o
LIBS = -L../StSoundLibrary -lstsound
CXXFLAGS = -I../StSoundLibrary -I../StSoundLibrary/LZH

ymplayer: $(PLAYEROBJS) libstsound.a
	$(CXX) -o ymplayer $(PLAYEROBJS) $(LIBS) -lasound -lncurses

libstsound.a:
	make -C ../StSoundLibrary
 
clean:
	rm -f *.o *~ ymplayer
