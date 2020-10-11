
**********************************
*  debian readme txt 2020-10-11  *
**********************************


================================================
wifi ipv6 SCU open

opkg update

opkg install 6relayd

6relayd -d -A eth2.2 br0
================================================
-------------------------------------------------------------------------------------------------------------

#开机自动安装运行 6relayd
export PATH='/etc/storage/bin:/tmp/script:/etc/storage/script:/opt/usr/sbin:/opt/usr/bin:/opt/sbin:/opt/bin:/usr/local/sbin:/usr/sbin:/usr/bin:/sbin:/bin'
export LD_LIBRARY_PATH=/lib:/opt/lib
while ! [ -x "`which opkg`" ]
do
        logger -t "【6relayd】" "Waitting opt install"     
        sleep 3
done
while ! [ -x "`which 6relayd`" ]
do
        logger -t "【6relayd】" "6relayd not found,begin to install it"
        opkg update
        opkg install 6relayd
done
logger -t "【6relayd】" "6relayd has been installed"
6relayd -d -A eth2.2 br0
logger -t "【6relayd】" "6relayd start"

------------------------------------------------------------------------------------------------------------------




usr -- Unix Software Resource

proteus


shell bash 

ctrl + w 往回删除一个单词，光标放在最末尾
ctrl + u 删除光标以前的字符
ctrl + k 删除光标以后的字符
ctrl + a 移动光标至的字符头
ctrl + e 移动光标至的字符尾
ctrl + l 清屏

C standard lib

/usr/include

ctags -R *


163mail

										SLL
POP3服务器: pop.163.com				端口：995
SMTP服务器: smtp.163.com				端口：25
IMAP服务器: imap.163.com				端口：993


zotero 数据迁移
storage 文件内容
zotero.sqllite文件移动

坚果云邮箱：seanchristspc@gmail.com

com.meizu.flyme.update


git 设置和取消代理

	设置代理：
		git config --global https.proxy http://127.0.0.1:1080
		git config --global https.proxy https://127.0.0.1:1080
		git config --global http.proxy 'socks5://127.0.0.1:1080'
		git config --global https.proxy 'socks5://127.0.0.1:1080'
	取消代理
		git config --global --unset http.proxy
		git config --global --unset https.proxy
	查询代理
		//查询全局代理
		git config --global http.proxy
		//查询局部代理
		git config --local http.proxy


vim tip

normal mode 
gf ---> file jump
gx ---> link jump

:Vex  ---> newtr

vim
undo -----> u
redo -----> Ctr-r
undo line ----> U

插入当前文件名
insert mode
Ctr-r ----> %

tip

:set nu
:set relativenumber

UltiSnips option for the snippet

snippet keyword "description" option
content
endsnippet

b — snippet can only be expanded if it’s the beginning of the line
A — snippet will be expanded automatically
w — snippet can be expanded if it’s a “word” to vim (check :help iskeyword). For example, a word can be “a sequence of other non-blank characters” according to :help word.
i — snippet can be expanded in the middle of a word.




权限管理

chgrp ---->  改变用户组
chown ---->  改变用户
chmod ---->  改变权限





linux screenshot 
Flameshot 

linux meeting
Terms

sha256 check command
md5sum filename
sha1sum filename	--> not recommend
sha256sum filename

docear 引入项目需要重启docear才可更新

手机开放adb端口
5555




