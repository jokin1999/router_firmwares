## 过渡固件

打开telnet连接

cd /tmp

wget http://192.168.2.113/openwrt-k2t-initramfs-factory-uboot-unlock.bin

mtd -r write /tmp/openwrt-k2t-initramfs-factory-uboot-unlock.bin firmware

## breed

登录后台

管理权页面打开ssh/root

scp连接/tmp放入 breed-qca9563-phicomm-k2t.bin

登录ssh

mtd -r write /tmp/breed-qca9563-phicomm-k2t.bin u-boot

## openwrt

登录breed

刷入固件 openwrt-ath79-generic-phicomm_k2t-squashfs-sysupgrade.bin
