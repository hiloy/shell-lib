### mysql 相关

### kill mysql connect id
	mysqladmin -h127.0.0.1 -uusername -ppassword pr //功能类似 show processlist;
	mysqladmin -h127.0.0.1 -uusername -ppassword pr|grep $1|grep $2|awk '{print $2}' > kill.list
	cat kill.list|xargs -n1 mysqladmin -h127.0.0.1 -uusername -ppassword kill

### 修改mysql auto_increment 初始值
    alter table tableName auto_increment = 1;

### mysql 设置和取消输出文件
说明：tee 设置 untee 删除
    tee logname
    untee

