### mysql 相关

### kill mysql connect id
mysqladmin -h*.*.*.* -uusername -ppassword pr //功能类似 show processlist;
mysqladmin -h*.*.*.* -uusername -ppassword pr|grep $1|grep $2|awk '{print $2}' > kill.list
cat kill.list|xargs -n1 mysqladmin -h*.*.*.* -uusername -ppassword kill
