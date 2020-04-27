git clone git@bitekda.co.kr:dhshin/shilla_security_monitor.git


git config --global user.email "dhshin@bitek.co.kr"
git config --global user.name "dhshin"

## gitlab 설정으로 안됨
git remote add gitlab https://server/namespace/project.git


```
git remote add origin http://bitekda.co.kr:8001/dhshin/shilla_security_monitor.git
```


# 에러 조치
```
error code

fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.


Please make sure you have the correct access rights
and the repository exists.

git remote -v

-기존 원격저장소 연결 삭제

Git remote remote 몽키xxxx

git remote remove gitlab

git push -u origin master
```
