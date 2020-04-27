# bitek_study


## setting
```
git clone http://bitekda.co.kr/dhshin/bitek_study.git
```


Command line instructions
You can also upload existing files from your computer using the instructions below.


Git global setup
git config --global user.name "dhshin"
git config --global user.email "dhshin@bitek.co.kr"

Create a new repository
git clone git@bitekda.co.kr:dhshin/bitek_study.git
cd bitek_study
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master

Push an existing folder
cd existing_folder
git init
git remote add origin git@bitekda.co.kr:dhshin/bitek_study.git
git add .
git commit -m "Initial commit"
git push -u origin master

Push an existing Git repository
cd existing_repo
git remote rename origin old-origin
git remote add origin git@bitekda.co.kr:dhshin/bitek_study.git
git push -u origin --all
git push -u origin --tags
