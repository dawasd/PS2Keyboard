# Custom fork notest:

## NoceMCU V2

Example platformio.ini env:

```
[env:nodemcuv2]
platform = espressif8266
board = nodemcuv2
build_flags =
	-D ESP8266
	-D NODEMCUV2
```
  
NODEMCUV2 is required to set ps2interrupt function to use ICACHE_RAM_ATTR.

Without ICACHE_RAM_ATTR, may get errors like:

```
ISR not in IRAM!

User exception (panic/abort/assert)
--------------- CUT HERE FOR EXCEPTION DECODER ---------------

Abort called

>>>stack>>>

ctx: cont
sp: 3ffffef0 end: 3fffffc0 offset: 0000
3ffffef0:  feefeffe feefeffe feefeffe feefeffe  
3fffff00:  000000fe 00000000 00000000 00000000
3fffff10:  00000000 00000000 00000000 00ff0000
3fffff20:  5ffffe00 5ffffe00 3ffe884e 3ffee614  
3fffff30:  00000000 00000002 00000004 4020216a
3fffff40:  4010041d 10428b1f ffffff00 4020217c
3fffff50:  402015a8 3ffe884d 00000004 4020267e  
3fffff60:  402015a8 3ffe884d 3ffee5ac 40201750
3fffff70:  3fffdad0 00000005 00000004 4020271c
3fffff80:  4020228d 000003e8 3ffee614 40201480
3fffff90:  3fffdad0 00000000 3ffee5ac 4020106c  
3fffffa0:  feefeffe feefeffe 3ffee600 40201cf8
3fffffb0:  feefeffe feefeffe 3ffe85d8 40100dad
<<<stack<<<

--------------- CUT HERE FOR EXCEPTION DECODER ---------------

 ets Jan  8 2013,rst cause:2, boot mode:(3,6)
```
  


# Original README:

#PS/2 Keyboard Library#

PS2Keyboard allows you to use a keyboard for user input. 

http://www.pjrc.com/teensy/td_libs_PS2Keyboard.html

![](http://www.pjrc.com/teensy/td_libs_PS2Keyboard.jpg)
