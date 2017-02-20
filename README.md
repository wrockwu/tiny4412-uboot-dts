tiny4412-uboot-dts
===
modified to support dts, which based on tiny4412 official u-boot.<br>

allocate image[8] to store dtb information.<br>

use command to build:<br>
make tiny4412_config<br>
make ARCH=arm CROSS_COMPILE=arm-none-linux-gnueabi- -j4<br>
make -C sd_fuse<br>

use command to make uImage<br>
./mkimage -n "linux-4.4" -A arm -O linux -T kernel -C none -a 0x40000800 -e 0x4000800 -d zImage uImage<br>


