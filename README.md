# zte-e8820v2

对于zet-e8820v2，谋求原版openwrt自行修改dts不是业余人士能干的，我努力了一个多星期宣告放弃，目前找到的可用代码库是siwind的，他已经增补了dts等文件，虽然代码库不如原始openwrt/openwrt那么新，但好用。


### 目前成果：

master版本编译正常，刷机能启动，运行良好。固件里只安装了kmod-usb-printer（我当ap用，还要连打印机），内核版本5.10.113，有r，无kv，可配置vlan。

19.07版本指定tag标签19.07.1代码库成功编译了固件，刷机后可运行，只是一直无法启动2g网络，剩余内存多了好几m，不过负载也高了几倍。不好用。试了试其他标签直接编译错误，死了1907版本的心了？

特别提出一点，menuconfig里我选了usb3支持，虽然这个机器硬件只是usb2，但选usb3才能成功识别usb打印机，我估计硬件芯片里是usb3的，外围缩水为usb2.


----------------------------------------------------------------------------
# zte-e8820s-spi

8820s为刷高恪硬改spi闪存，高恪玩够了，想刷回openwrt，我觉得改文件比改硬件方便些，所以。。。有了这。固件已经运行几天了，好用，内核版本5.10.113，有r，无kv，可配置vlan。另外预装的ddns、vlmcsd、SmartDNS，没有其他的了。代码库来源于siwind，是否有恶意代码我就没能力鉴别了。我试openwrt/openwrt指定分支，都没能成功。

SmartDNS在这个固件里一直显示收集数据，但dns功能没问题，网上也有人提出这个问题，估计luci不能适应最新的master源码，给作者去信了。
