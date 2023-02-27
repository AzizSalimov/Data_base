1. From the following table, write a SQL query to locate the detailsof customers with grade values above 100. Return customer_id, cust_name, city, grade, and salesman_id. 

# TASK1

```sql
select * from customer
where grade > 100
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221405655-64fe50ad-1744-474e-9b88-1d7ceb5b24e6.png)


2. From the following table, write a SQL query to find all the customers in ‘New York’ city who have a grade value above 100. Return customer_id, cust_name, city, grade, and salesman_id.   

# TASK2

```sql
select * from customer 
where city = 'New York' and grade > 100;
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221406052-9d1c9961-0f71-4b51-a692-053bc6c1c13f.png)

3. From the following table, write a SQL query to find customers who are from the city of New York or have a grade of over 100. Return customer_id, cust_name, city, grade, and salesman_id. 

# TASK3

```sql
select * from customer
where city = 'New York' or grade > 100
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221408464-e6f59cdc-5947-47b9-a89a-7a9eda7c773c.png)

4. From the following table, write a SQL query to find customers who are either from the city 'New York' or who do not have a grade greater than 100. Return customer_id, cust_name, city, grade, and salesman_id.  

# TASK4

```sql
select * from customer
where city = 'New York' or not grade > 100
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221409222-ee868e19-9e9d-4e81-8d67-872bf4fc323e.png)

5. From the following table, write a SQL query to identify customers who do not belong to the city of 'New York' or have a grade value that exceeds 100. Return customer_id, cust_name, city, grade, and salesman_id. 


# TASK5

```sql
select * from customer 
where not (city = 'New York' or grade > 100)
```

RESULT\


![изображение](https://user-images.githubusercontent.com/122611579/221471425-d41f6475-c175-4a4d-88fa-c8146899187a.png)
