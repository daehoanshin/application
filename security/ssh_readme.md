# client
ssh-keygen -t rsa

scp ~/.ssh/id_rsa.pub xbb123@sdhlab.com:id_rsa.pub

# server

id_rsa.pub open 

authorized_keys copy 편집