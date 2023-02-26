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

