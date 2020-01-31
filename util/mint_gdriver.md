
* 잘됨 [ExpanDrive](https://www.expandrive.com/welcome-to-expandrive/)







# h57 setting
마운트
./gdriver_start.sh

해지
fusermount -u /home/xbb123/google_driver


# google-drive-ocamlfuse
[google-drive-ocamlfuse](https://www.tecmint.com/mount-google-drive-in-linux-using-google-drive-ocamlfuse-client/2/)

[google-drive-ocamlfuse](https://github.com/astrada/google-drive-ocamlfuse)


```
sudo add-apt-repository ppa:alessandro-strada/ppa
sudo apt-get update
sudo apt-get install google-drive-ocamlfuse
mkdir ~/googleDrive && google-drive-ocamlfuse ~/googleDrive
```

If you have more than one account, you can run use following command.
```
google-drive-ocamlfuse -label label [mountpoint]
```
