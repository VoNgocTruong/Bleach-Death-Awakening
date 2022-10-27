OS：CentOS 7

DOWNLOAD https://mobaxterm.mobatek.net/ ĐỂ KẾT NỐI SSH.

LINK TOOL:

LINK SOURCE CÀI THỦ CÔNG:

LINK CentOS ĐÃ CÀI ĐẦY ĐỦ:

DOWNLOAD AAPANEL.
- yum install -y wget && wget -O install.sh http://www.aapanel.com/script/install_6.0_en.sh && bash install.sh

DOWNLOAD 4 THỨ CẦN THIẾT SAU KHI LOGIN VÀO AAPANEL ↧

- ngx 1.18
- mysql 5.6
- php 5.6
- phpmyadmin 4.9

ALLOW PORT RANGE VỚI FIREWALLD

RANGE -> 1:65535

- firewall-cmd --add-port=1-65535/tcp --permanent
- sudo firewall-cmd --reload
- check stat port firewall-cmd --list-ports

TẮT FIREWALLD
- systemctl stop firewalld.service
- systemctl disable firewalld.service

==> DONE SETUP CentOS

UPLOAD sishen.zip TRONG FOLDER SOURCE GAME LÊN CentOS Ở FOLDER / (ROOT)

GIẢI NÉN

- cd / && unzip sishen.zip

CẤP QUYỀN

- chmod -R 7777 /data/
- chmod -R 7777 /www/wwwroot

DOWNLOAD JAVA

- yum install java-1.8.0-openjdk\* -y
- yum install jsvc

QUAY LẠI TRANG AAPANEL -> ADD WEBSITE (Ở NAVBAR) -> ADD SITE {IP:81} -> WEBSITE PATH ↧

\www\wwwroot\sishen

CLICK DATABASES (Ở NAVBAR) SET PASS ROOT：123456

CLICK APP STORE (Ở NAVBAR) -> INSTALLED -> SETTING CỦA MYSQL -> CLICK CONFIG (HÀNG 2)

TÌM DÒNG 26 VÀ ADD lower_case_table_names=1

SAU ĐÓ CLICK SERVICE -> RELOAD -> RESTART

IMPORT DATABASE (HƠI LÂU CHÚT)

- cd /data && ./sk

EDIT LẠI IP SERVER THEO LINK DƯỚI (VÀO AAPANEL -> FILE)

/www/wwwroot/sishen/ServerList.txt

==> DONE SETUP SERVER GAME

START SERVER GAME

- cd /data/ss/public && sh start.sh start
- cd /data/ss/server && sh start.sh start

STOP SERVER GAME

- cd /data/ss/public && sh start.sh stop
- cd /data/ss/server && sh start.sh stop

SETUP IP CLIENT GAME (APK)
IP CỦA MÌNH: 192.168.136.129

DÙNG APK Easy DECOMPILE FILE APK GAME SAU ĐÓ THEO ĐƯỜNG DẪN CUT FILE assets.resources.prefabs.global.global.gamemanager
RA NGOÀI CHỖ KHÁC
assets\AssetBundles\rcj_lhsl_fb1\assets.resources.prefabs.global.global.gamemanager

MỞ AssetBundleExtractor.exe  

CHỌN 文件 - 打开 CHỌN assets.resources.prefabs.global.global.gamemanager

CHỌN 信息 VÀ TÌM ID：2027190313729920672 MonoBehaviour

XUẤT FILE CHỌN 导出,转存 XUẤT DẠNG TXT ĐỂ EDIT IP

ĐỔI ALL IP:192.168.136.129

QUAY TRỞ LẠI MonoBehaviour 点击 - 导入转存 - 选择那个 txt 文件 - 确定 - 是 ，

然后点击软件 - 文件 - 保存 - 2，

最后软件点击 文件 - 压缩 - 选择 2 - 提示不理 确定 - 保存为 assets.resources.prefabs.global.global.gamemanager -

NÉN XONG LẠI FILE THÀNH 19KB VÀ CUT NÓ VỀ FOLDER Ở BƯỚC ĐẦU

COMPILE LẠI THÀNH APK Ở APK Easy

VÀO ApkToolAid ĐỂ SIGNED APK

TRANG GM:
http://IP:81/gm/gm.php
授权码：ymdog.cn
