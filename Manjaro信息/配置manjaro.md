安装 搜狗输入法
sudo pacman -S fcitx-im
sudo pacman -S fcitx-configtool
yay fcitx-sogoupinyin
添加输入法配置文件，输入命令：
sudo vim ~/.xprofile
编辑模式写入：
export GTK_IM_MODULE=fcitx
export QT_IM_MODULE=fcitx
export XMODIFIERS="@im=fcitx"
fcitx配置

sudo pacman -S mysql
sudo mysql_install_db --user=mysql --basedir=/usr --datadir=/var/lib/mysql
sudo systemctl start mysqld
sudo mysql_secure_installation
sudo systemctl enable mysqld
mysql -u root -p

qt开发
安装
sudo pacman -Sy make cmake git
