tiny4412-uboot-dts
===
This uboot is based on tiny4412 official u-boot.<br>

#new feature
1.support dts.repartition, add image[8] to store dtb information.<br>
2.modify boot_args to support linux boot.<br>
3.support ramdisk rootfs.<br>
4.supprot uImage type kernel.<br>

#usefull commands<br>
command to build:<br>
make tiny4412_config<br>
make ARCH=arm CROSS_COMPILE=arm-none-linux-gnueabi- -j4<br>
make -C sd_fuse<br>

command to make uImage<br>
./mkimage -n "linux-4.4" -A arm -O linux -T kernel -C none -a 0x40000800 -e 0x4000800 -d zImage uImage<br>


