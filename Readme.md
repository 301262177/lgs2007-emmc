# 借助 GitHub Actions 的 OpenWrt 在线自动编译.

#### hanwckf大佬mt798x闭源仓库- [hanwckf/immortalwrt-mt798x](https://github.com/hanwckf/immortalwrt-mt798x).

#### 237大佬mt798x闭源仓库- [padavanonly/immortalwrt-mt798x](https://github.com/padavanonly/immortalwrt-mt798x).

#### 237大佬mt798x-23.05闭源仓库-[padavanonly/immortalwrt-mt798x-23.05](https://github.com/padavanonly/immortalwrt-mt798x-23.05).

#### hanwckf大佬mt798x uboot仓库- [hanwckf/bl-mt798x](https://github.com/hanwckf/bl-mt798x).

### 刷砖也不怕！可以通过串口救砖：[MediaTek Filogic 系列路由器串口救砖教程](https://www.cnblogs.com/p123/p/18046679)
---

- #### 说明

- #### 1. Choose mt_wifi/warp firmware

- #### 2. Not build luci-app-dockerman
该选项默认关闭，即按.mtwifi-cfg.config配置文件编译dockerman，不需要编译dockerman请打钩。  
.mtwifi-cfg.config配置文件中已设置编译dockerman：  
CONFIG_PACKAGE_luci-app-dockerman=y  

---
## CMCC-RAX3000M-eMMC/CMCC-XR30-eMMC workflow 手动运行可选项：
- [x] Use nx30pro eeprom and fixed WiFi MAC address
- [ ] Use luci-app-mtk wifi config
- [ ] Not build luci-app-dockerman
  

- #### 3. Use nx30pro eeprom and fixed WiFi MAC address
该选项默认开启，即使用nx30pro的高功率eeprom，不需要请取消打钩。（237大佬2024/8/2日eeprom）  
不使用独立fem无线功放的MT7981B路由器可以通过替换高功率的eeprom提高信号强度。  
RAX3000M/XR30的factory eeprom设置功率不高，2.4G是23dBm、5G是22dBm，使用NX30 PRO的高功率eeprom，2.4G可提升至25dBm、5G提升至25dBm。  
开启该选项会使用NX30 PRO的eeprom替换掉固件中的MT7981_iPAiLNA_EEPROM.bin文件，并将facotry分区读取的MAC写入到dat以便固定WiFi MAC。  


- #### 4. Not build luci-app-dockerman
该选项默认关闭，即按.mtwifi-cfg.config配置文件编译dockerman，不需要编译dockerman请打钩。  
.mtwifi-cfg.config配置文件中已设置编译dockerman：  
CONFIG_PACKAGE_luci-app-dockerman=y  

---
### 感谢P3TERX的Actions-OpenWrt
- [P3TERX](https://github.com/P3TERX/Actions-OpenWrt)
[Read the details in my blog (in Chinese) | 中文教程](https://p3terx.com/archives/build-openwrt-with-github-actions.html)
### 感谢237176253的immortalwrt-21.02和23.05源码
- [237176253](https://github.com/padavanonly/immortalwrt-mt798x)
- [237176253](https://github.com/padavanonly/immortalwrt-mt798x-23.05)
### 感谢hanwckf的immortalwrt-21.02源码
- [hanwckf](https://github.com/hanwckf/immortalwrt-mt798x)
### 感谢lgs2007m的项目
- [lgs2007m](https://github.com/lgs2007m/Actions-OpenWrt)
