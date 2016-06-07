### mysql 相关

### kill mysql connect id
	mysqladmin -h127.0.0.1 -uusername -ppassword pr //功能类似 show processlist; 
	mysqladmin -h127.0.0.1 -uusername -ppassword pr|grep $1|grep $2|awk '{print $2}' > kill.list 
	cat kill.list|xargs -n1 mysqladmin -h127.0.0.1 -uusername -ppassword kill
