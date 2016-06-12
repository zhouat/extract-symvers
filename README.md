# extract-symvers
Extract Module.symvers info from a binary kernel

ls -l /dev/block/platform/msm_sdcc.1/by-name/
abootimg
abootimg -x boot.img

python extract-symvers.py -B c0008000[dmesg | grep '\.text' --color=auto] zImage > Module.symvers
