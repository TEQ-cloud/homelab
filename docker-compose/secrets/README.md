# Secrets Folder
The 'secrets' folder is used to house all the text files containing secrets like passwords and encryption keys, on a per secret basis. These text files are later used bij Docker Compose to create the secrets containers use on runtime.  

An example of such a file will be a file named 'containername_mysql_password.txt' containing the password string like:
```
th3p@55w0rd1u53f0rmysql
```