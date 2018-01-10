# scut626
## 普通
/home/scut_626/anaconda3/bin/gpustat  | bash /home/scut_626/status-gpu/ansi2html.sh > /home/scut_626/status-gpu/index.html

/home/scut_626/anaconda3/bin/gpustat --color  | bash /home/scut_626/status-gpu/ansi2html.sh > /home/scut_626/status-gpu/index.html
cat /home/scut_626/anaconda3/bin/gpustat --color > /home/scut_626/status-gpu/1

## crontab
*/10 * * * * cat /home/scut_626/anaconda3/bin/gpustat -pcu > /home/scut_626/status-gpu/116.57.86.56
*/10 * * * * cat /home/scut_626/status-gpu/116* | /home/scut_626/status-gpu/ansi2html.sh >  /home/scut_626/status-gpu/index.html


# 服务器
## 普通
cat /home/lab-huang.zhongyi/software/gpu-status/1* | bash /home/lab-huang.zhongyi/software/gpu-status/ansi2html.sh > /home/lab-huang.zhongyi/software/gpu-status/index.html

/home/lab-huang.zhongyi/.local/bin/gpustat --color  | bash /home/lab-huang.zhongyi/software/gpu-status/ansi2html.sh > /home/lab-huang.zhongyi/software/gpu-status/index.html
cat /home/lab-huang.zhongyi/.local/bin/gpustat --color  > /home/lab-huang.zhongyi/software/gpu-status/1

# 安装环境
wget http://www.pixelbeat.org/scripts/ansi2html.sh
pip install gpustat
sudo apt-get install gawk apache2 libapache2-mod-php php php-mysql php-json mysql-server


# nmap
##server
nmap 116.57.86.156-159 116.57.86.151-154 -p 22 | bash ./ansi2html.sh > /var/www/html/index.html
##crontab
* * * * * /usr/bin/nmap 116.57.86.156-159 116.57.86.151-154 -p 22 | bash /home/scut_626/status-gpu/ansi2html.sh >  /var/www/html/index.html
## All server
nmap 116.57.86.156-159 116.57.86.151-154 -p 22
## only CPU server:
nmap 116.57.86.151-154 -p 22
## only GPU server:
nmap 116.57.86.156-159 -p 22


# natapp
nohup ./natapp -authtoken=644b1480958a7551 -log=stdout &
ps -ef|grep natapp
kill -9 ID


# teamviewer密码
392088179
scut_626