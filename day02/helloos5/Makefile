# ファイル生成規則
ipl.bin : ipl.nas Makefile
	../../tools/nask.exe ipl.nas ipl.bin ipl.lst

#helloos.img : ipl.bin tail.bin Makefile
helloos.img : ipl.bin Makefile
	type ipl.bin > helloos.img

asm :
	../../tools/make.exe -r ipl.bin

img :
	../../tools/make.exe -r helloos.img

run :
	../../tools/make.exe img
	../../tools/qemu/qemu-system-i386.exe helloos.img

clean :
	-del ipl.bin
	-del helloos.img