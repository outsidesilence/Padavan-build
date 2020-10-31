# Padavan-build说明  
- 基于 chongshengB 项目修改。  
- 完全精简了插件和系统组件，只保留了ssh、smartdns、frp、zerotier。其中smartdns更新到官网3.3版，即2020/9/8版。  
- C大 smartdns配置脚本有bug，web控制台smartdns界面，IPV6解析选项点击打开或关闭按钮均无效。研究了下大概是1、配置文件里的snds_ipv6与后台的sdns_ipv6变量名反了。2、前端可以读取到后台snds_ipv6的值，但是修改配置后点击应用配置无效。估计是applyRule()方法里的某个写入函数有问题。所以根据自己的需求修改了smartdns_conf脚本和smartdns_custom脚本。
