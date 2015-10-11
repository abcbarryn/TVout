This branch of the TVout library has been patched to allow use with the Arduino Leonardo.
The goal of this project is to create a simple interupt driven library for generating composite video on a single AVR chip.

Currently the output is NTSC or PAL at a resolution of 128x96 by default. The library currently works on ATmega168,328,1280,2560,644p,1284p,32U4,AT90USB1286 and more can be added by editing spec/hardware_setup.h.

There are some timing issues with the m1284p, may be related to sanguino core.

```
MCU         SYNC	VIDEO	AUDIO	Arduino	        SYNC	VIDEO	  AUDIO
m168,m328	B 1	    D 7	    B 3	    NG,Decimila,UNO	9	    7	      11
m1280,m2560	B 5	    A 7	    B 4	    Mega            11	    A7(D29)	  10
m644,m1284p	D 5	    A 7	    D 7	    sanguino        13	    A7(D24)	  8
m32u4       B 5	    B 4	    B 7	    Leonardo        9       8         11
AT90USB1286	B 5	    F 7	    B 4	    --	            --	    --	      --
```
