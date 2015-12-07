# DevOps
Devops
## SSH
1. Generate a new SSH key:
```ssh-keygen -t rsa -b 4096 -C "your_email@example.com" ```
2. Copy the contents of the id_rsa.pub file to your clipboard:
```pbcopy < ~/.ssh/id_rsa.pub ```


## Hadoop
1. Show the file ```hdfs dfs -ls ```
2. Copy from local  ```hdfs dfs -copyFromLocal  file.csv ```
3. Using Sqoop with Mysql  ```sudo service mysqld status ```
4. Login to myql ``` mysql -u root -p ```
5. Show DB ```show databases ; ```
6. Exit, ```exit ```
7. Import data from mysql to hdfs using Sqoop 
8. ``` sqoop import \
--connect jdbc:mysql://127.0.0.1:3306/retail_db \
--table products \
--username root -P \
--direct -m 1;   ```
9. See the results: ```hdfs dfs -ls products```
10. Delete this folder ```hdfs dfs -rm -r products ```
11. Add data using Hive with the table name myProducts ``` sqoop import \
--connect jdbc:mysql://127.0.0.1:3306/retail_db \
--table products \
--username root -P \
--hive-import \
--hive-table myProducts \
--direct -m 1; ```
12. See the results using Hue in the file browser under user Hive 
13. ```/ user/ hive/ warehouse/ myproducts/ ```
13. See the result of Hive using Hive query: ```select * from myProducts  limit 10; ```
14. 




More info :<br>
https://help.github.com/articles/generating-ssh-keys/
