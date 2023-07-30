CXX ?= g++

all: ymplayer ym2wav

PLAYEROBJS = sound.o ui.o ymplayer.o
CONVOBJS = ym2wav.o

LIBS = -L../StSoundLibrary -lstsound
CXXFLAGS = -O2 -I../StSoundLibrary -I../StSoundLibrary/LZH

ymplayer: $(PLAYEROBJS) ../StSoundLibrary/libstsound.a
	$(CXX) -o ymplayer $(PLAYEROBJS) $(LIBS) -lasound -lncurses

ym2wav: $(CONVOBJS) ../StSoundLibrary/libstsound.a
	$(CXX) -o ym2wav $(CONVOBJS) $(LIBS) -lasound -lncurses

../StSoundLibrary/libstsound.a:
	make -C ../StSoundLibrary
 
clean:
	rm -f *.o *~ ymplayer
