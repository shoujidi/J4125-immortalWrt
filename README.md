J4125-8125 四网口专用固件

## 🤔 这是什么？
它是一个工作流。可快速构建 带docker且支持自定义固件大小的 immortalWrt
> 1、支持自定义固件大小 默认1GB 不建议设置过大 推荐1G-2G 更大需求可通过自定义插件里的扩容插件自行扩容<br>
> 2、支持可选预安装docker（可选）支持在UI上勾选是否集成商店<br>
> 3、支持按需增加[第三方软件](https://github.com/wukongdaily/store/blob/master/README.md)  如何集成 https://github.com/wukongdaily/AutoBuildImmortalWrt/discussions/209 <br>
> 4、点击这里查看👉🏻[全部支持的机型列表](https://github.com/wukongdaily/AutoBuildImmortalWrt/blob/master/SUPPORT.md) 👈🏻<br>
> 5、在UI上 新增luci版本的可选项，默认最新版24.10.4 https://github.com/wukongdaily/AutoBuildImmortalWrt/discussions/426<br>
> 6、支持设置管理地址的ip 比如192.168.100.1 这里强调 这项功能仅针对多网口机型 单网口的逻辑还是自动获取ip模式（dhcp）无固定ip<br>
> 7、对于[插件追新的用户 建议前往run项目 下载run后 ](https://github.com/wukongdaily/RunFilesBuilder/discussions/41)用命令sh xx.run 覆盖安装 <br>

## [基本用法步骤](https://github.com/wukongdaily/AutoBuildImmortalWrt/wiki) 👈🏻
1、fork本项目<br>
2、在fork后的项目中 点击【action】 找到需要的工作流后 run-workflow<br>


## 如何查询imm仓库内有哪些插件
https://mirrors.sjtug.sjtu.edu.cn/immortalwrt/releases/24.10.4/packages/x86_64/luci/
## 如何查询imm仓库外目前可以集成哪些插件
https://github.com/wukongdaily/store
> 具体方法 https://github.com/wukongdaily/AutoBuildImmortalWrt/discussions/209
## 【视频教程】如何集成第三方插件？
https://www.youtube.com/watch?v=KN6AJYV1hBI <br>
https://www.youtube.com/watch?v=7i6BQeitUtE


## 正常路由模式必读
所谓正常的路由模式 就是指多网口用户，多网口的意思就是2个或者2个以上网口的情况。<br>
一般wan用于拨号或者自动获取ip <br>
而其他lan一般是给其他设备分配dhcp<br>
这种情况下 你可以修改路由器的默认ip  `192.168.100.1` 比如你可以修改为`192.168.80.1 ` 诸如此类。<br>
没错，修改此ip 无非就是为了避免跟光猫或者跟家庭中的其他路由器网段冲突。大多数用户，无需更改。

## 该固件默认属性？(必读)
- 该固件刷入【单网口设备】默认采用DHCP模式,自动获得ip。类似NAS的做法
- 该固件刷入【多网口设备】默认WAN口采用DHCP模式，LAN 口ip为  `192.168.100.1` <br>其中eth0为WAN 其余网口均为LAN
- 若用户在工作流中勾选了拨号信息 则WAN口模式为pppoe拨号模式。
- 建议拨号用户使用之前重启一次光猫。
- 综合上述特点，【单网口设备】应该先接路由器，先在上级路由器查看一下它的ip 再访问。
- 上述特点 你都可以通过 `99-custom.sh` 配置和调整



## ❤️其它GitHub Action项目推荐🌟 （建议收藏）⬇️
- ### [一键生成run插件] 🆕
- https://github.com/wukongdaily/RunFilesBuilder<br>
- ### [一键生成docker离线镜像] 🆕
- https://github.com/wukongdaily/DockerTarBuilder<br>
- ### [OpenWrt/Armbian IMG安装器ISO] 🆕
- https://github.com/wukongdaily/img-installer


## ❤️如何构建docker版ImmortalWrt（建议收藏）⬇️
https://wkdaily.cpolar.cn/15
# 🌟鸣谢
### https://github.com/immortalwrt
### https://github.com/ophub/flippy-openwrt-actions
### https://github.com/ophub/amlogic-s9xxx-openwrt
### https://github.com/sirpdboy
### https://github.com/wukongdaily/ib-overlay
### 高级卸载插件出处 by VedioTalk https://xz.vumstar.com
### 新增极光主题 来自 https://github.com/eamonxg/luci-theme-aurora
### 新增Bandix流量监控 来自 https://github.com/timsaya/luci-app-bandix
### 新增rtp2httpd 来自https://github.com/stackia/rtp2httpd





<details>
<summary><h2>🍭相关引用</h2></summary>

#### 🍭引用和项目参考的仓库
- https://github.com/wukongdaily/RunFilesBuilder
- https://github.com/wukongdaily/store
- https://github.com/xiaorouji/openwrt-passwall
- https://github.com/xiaorouji/openwrt-passwall2
- https://github.com/sirpdboy/luci-theme-kucat
- https://github.com/AdguardTeam/AdGuardHome
- https://github.com/kiddin9/kwrt-packages
