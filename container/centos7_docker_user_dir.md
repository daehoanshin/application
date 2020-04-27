[docker 기본디렉토리 변경](http://www.kwangsiklee.com/2017/07/docker-%EC%95%88%EC%93%B0%EB%8A%94-%EB%8D%B0%EC%9D%B4%ED%84%B0-%EC%A0%95%EB%A6%AC%ED%95%98%EA%B8%B0/)

$ vi /lib/systemd/system/docker.service
[Service]
...
ExecStart=/usr/bin/docker daemon -g /원하는디렉토리
$ sudo service docker stop
$ sudo systemctl daemon-reload
$ sudo service docker start
