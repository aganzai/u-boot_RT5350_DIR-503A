# u-boot_RT5350_DIR-503A
# http://www.aganzai.com

1 config uboot
make menuconfig
select Chip ID RT5350
select DRAM Component 512Mb (as your DRAM)

2 build uboot
use openwrt CROSS_COMPILE
STAGING_DIR=$PWD/../../openwrt/barrier_breaker/staging_dir/ make  CROSS_COMPILE=$PWD/../../openwrt/barrier_breaker/staging_dir/toolchain-mipsel_24kec+dsp_gcc-4.8-linaro_uClibc-0.9.33.2/bin/mipsel-openwrt-linux-

3 run in ram
