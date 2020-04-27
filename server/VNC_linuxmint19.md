
# x11vnc
```
sudo apt-get -y remove vino
sudo apt-get -y install x11vnc
sudo mkdir /etc/x11vnc
sudo x11vnc --storepasswd /etc/x11vnc/vncpwd

sudo vi /etc/x11vnc/vncpwd
sudo vim /etc/x11vnc/vncpwd
```


`sudo vim /lib/systemd/system/x11vnc.service`


```
[Unit]
Description=Start x11vnc at startup.
After=multi-user.target


[Service]
Type=simple
ExecStart=/usr/bin/x11vnc -auth guess -forever -noxdamage -repeat -rfbauth /etc/x11vnc/vncpwd -rfbport 5900 -shared


[Install]
WantedBy=multi-user.target
```


#  재시작
```
sudo systemctl stop x11vnc.service
sudo systemctl start x11vnc.service
```

```
sudo systemctl daemon-reload
sudo systemctl enable x11vnc.service


```




# 참고 vnc4server 안됨
```sudo apt install vnc4server -y
vncpasswd
vncserver :1
vncserver -kill :1
vi .vnc/xstartup
vncserver :1 -geometry 800x600 -depth 24
history
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTk2Nzk5MzQ2XX0=
-->
