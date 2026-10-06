# RAX3000M NAND — padavanonly 6.6 闭源驱动固件 (GitHub Actions)

一键云编译 **CMCC RAX3000M NAND(普通版)** 的 ImmortalWrt 固件:

- 源码:[padavanonly/immortalwrt-mt798x-6.6](https://github.com/padavanonly/immortalwrt-mt798x-6.6),分支 `openwrt-24.10-6.6`(内核 6.6,**闭源 mt_wifi 驱动**,WPA3 / HNAT / WED)
- 仅编译单台设备:`cmcc_rax3000m-nand`(见 `rax3000m-nand.config`,由上游 `defconfig/mt7981-ax3000.config` 过滤而来)
- 触发:仓库 Actions 页面 → **Run workflow**
- 产物:Actions artifact `rax3000m-nand-6.6-closed`,含镜像与 `sha256sums.txt`,保留 90 天

## 刷机提醒
- 仅适用于 **NAND(普通版)** 机器;emmc 版请勿使用。
- 跨驱动(开源 mt76 → 闭源 mt_wifi)建议 `sysupgrade -n` 清配置刷入;刷前先 `sysupgrade -b` 备份。
- 首次编译约 1.5~3.5 小时。
