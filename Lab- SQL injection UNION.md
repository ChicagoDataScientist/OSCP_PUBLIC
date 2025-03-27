up:[[WebSecurityAcademy]] #sqlinjection

# Lab: SQL injection UNION
The goal is to find how many columns are in the SQL Table

[Click here for lab](https://portswigger.net/web-security/sql-injection/union-attacks/lab-determine-number-of-columns)

First, access the target web page in the Burpsuite Browser

![[Pasted image 20240612150401.png]]

Click on a category to create an sql query. Here, I selected "gifts"

Here is the "gifts" page

![[Pasted image 20240612150517.png]]



![[Pasted image 20240612150920.png]]
You can see the "Gifts" filter from the SQL Query created

RIght click on that and select "send to repeater"
![[Pasted image 20240612151116.png]]

![[Pasted image 20240612151226.png]]

add a single quote ' to see if there is an sql injection vulnerability

![[Pasted image 20240612151617.png]]

Here you see the error you are looking for




Now, test to see how many columns are in the sql table:  We enter ```
```
Gifts'+UNION+SELECT+NULL-- HTTP/2
```

We replace space with + for the web query.

![[Pasted image 20240612152154.png]]

We see we did not get the right amount of columns because we get a 500 error.  We will try to add another column to our query.

![[Pasted image 20240612152343.png]]

We still get the same error. Two columns is not enough.  We need to try again!

![[Pasted image 20240612152504.png]]

We get an "HTTP OK" with three NLL columns.  We have solved the lab!

![[Pasted image 20240612152810.png]]

When we render the page, we see we have broken in to the sql code!

