O = bgmlist.o brr.o ctrltbl.o help.o inst.o loadrom.o main.o metadata.o midi.o misc.o packlist.o packs.o parser.o play.o ranges.o resource.o song.o songed.o sound.o text.o tracker.o
CC = x86_64-w64-mingw32-gcc -DDEBUG -Os -W -Wall -std=gnu99

a.exe: $O
	x86_64-w64-mingw32-gcc -mwindows -s -fno-exceptions $O -lcomctl32 -lcomdlg32 -lgdi32 -lwinmm -Wl,ldscript
	
resource.o: resource.rc
	windres $< -o $@

clean:
	rm *.o