# Hheretic
A port of Hhexen v1.6.4 from https://hhexen.sourceforge.net/hhexen.html for miyoo cfw

# Keymap
*NOTE: due to weapon have 4 slots, use combo keys to switch slot manual from 1 to 4, 
~~~
Up : go ahead
Down: step back
Right: look to the right
Left: look to the left
A: fire
B: strafe
	(B + Left: strafe left)
	(B + Right: strafe right)
X: use
Y: jump
Reset: open map
L + Left: move selection inventory to left
L + RIGHT: move selection inventory to right
L + Up: fly up
L + Down: fly down
R + Left: switch weapon slot down (default is slot 2)
R + Right: switch weapon slot up (inscrease slot number)
R + Up: look up
R + Down: look down
~~~
# How to build
You need docker, debian linux or arch linux
~~~
# if you first time build code, run this command to set up toolchain
docker pull miyoocfw/toolchain-shared-uclibc:latest

# to compile
docker run --volume ./:/src/ -it miyoocfw/toolchain-shared-uclibc:latest
cd src
./configure --disable-gl --enable-fullscreen --host=arm-linux CC=arm-linux-gcc
make -j $(nproc)
~~~

# WAD file info:

1.0 wads:
  b2543a03521365261d0a0f74d5dd90f0  hexen.wad (20,128,392 bytes)
  1077432e2690d390c256ac908b5f4efa  hexdd.wad ( 4,429,700 bytes)

1.1 wads:
  abb033caf81e26f12a2103e1fa25453f  hexen.wad (20,083,672 bytes)
  b68140a796f6fd7f3a5d3226a32b93be  hexen.wad (21,078,584 bytes -- Mac version)
  78d5898e99e220e4de64edaa0e479593  hexdd.wad ( 4,440,584 bytes)

Demo wad 1.0 (from PC shareware hexndemo.zip):
  876a5a44c7b68f04b3bb9bc7a5bd69d6  hexen.wad (10,644,136 bytes)

Demo wad 1.1 (from Macintosh shareware MacHexenDemo.hqx):
  925f9f5000e17dc84b0a6a3bed3a6f31  hexen.wad (13,596,228 bytes)