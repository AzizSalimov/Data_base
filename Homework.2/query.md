1.Write a SQL statement that displays all the information about all salespeople. 

# TASK1

```sql
select * from salesman;
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221350132-85c9d23a-f34d-4299-9228-21d4ebba9dba.png)



2. Write a SQL statement to display a string This is SQL Exercise, Practice and Solution. 

# TASK2

```sql
select 'This is SQL Exercise, Practice and Solution';
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221350078-8daa773f-e04d-4c1f-bd62-71c047b38035.png)

3. Write a SQL query to display three numbers in three columns.

# TASK3

```sql
select 10 , 15, 20

```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221351621-f8323b9e-9ab0-4f26-9fb8-6411c4232b18.png)

4. Write a SQL query to display the sum of two numbers 10 and 15 from the RDBMS server.

# TASK4

```sql
select 10 + 15
```
RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221351715-166c5b1b-16c6-417b-8d13-f147eb880d44.png)

5. Write an SQL query to display the result of an arithmetic expression.

# TASK5

```sql
select 10 * 10 + 5 * 5
```
RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221352231-bc23817d-f6dc-4463-8b50-2cdf25712055.png)


6. Write a SQL statement to display specific columns such as names and commissions for all salespeople. 

# TASK6

```sql
select name, commission from salesman
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221352913-911b964b-a950-40d2-9f6b-d150d9e7a642.png)

7. Write a query to display the columns in a specific order, such as order date, salesman ID, order number, and purchase amount for all orders.  

# TASK7

```sql
select ord_data, selesman_id, ord_no, purch_amt from orders
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221354514-b918003d-7386-4c12-94d5-ac374034faaf.png)

From the following table, write a SQL query to identify the unique salespeople ID. Return salesman_id.

# TASK8

```sql
select distinct salesman_id from orders
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221356241-9f87304b-7ef2-431c-8284-cb16baf12d56.png)


9. From the following table, write a SQL query to locate salespeople who live in the city of 'Paris'. Return salesperson's name, city. 

# TASK9

```sql
select name, city from salesman 
where city= 'Paris'
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221356476-e4d2250c-6c25-419a-ae00-a745c70b80be.png)


10. From the following table, write a SQL query to find customers whose grade is 200. Return customer_id, cust_name, city, grade, salesman_id. 

# TASK10

```sql
select * from customer 
where grade= 200
```
RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221356586-d1aec270-fa35-4363-90ba-02d594aaea1a.png)


11. From the following table, write a SQL query to find orders that are delivered by a salesperson with ID. 5001. Return ord_no, ord_date, purch_amt

# TASK11

```sql
select ord_no, ord_date, purch_amt from orders
where salesman_id= 5001
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221393757-71920c7b-3d11-4222-aa03-d86f76bbde65.png)

12. From the following table, write a SQL query to find the Nobel Prize winner(s) for the year 1970. Return year, subject and winner.  

# TASK12

```sql
select year, subject, winner from nobel_win
where year = 1970
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221393959-36624974-2474-4d92-803f-70e20b6ad4eb.png)


13. From the following table, write a SQL query to find the Nobel Prize winner in ‘Literature’ for 1970. Return winner. 


# TASK13

```sql
select year, subject, winner from nobel_win
where year = 1971 and subject = 'Literature'
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221394256-c8dd576a-bc37-42d6-8dba-16cd5c590c94.png)

14. From the following table, write a SQL query to locate the Nobel Prize winner ‘Dennis Gabor'. Return year, subject. 

# TASK14

```sql
select winner, year, subject from nobel_win
where winner = 'Dennis Gabor'
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221394666-754896a2-8506-4006-b597-275c1026e3ae.png)


15. From the following table, write a SQL query to find the Nobel Prize winners in the field of ‘Physics’ since 1950. Return winner.  


# TASK15

```sql
select year, subject, winner from nobel_win
where year >= 1950 and subject = 'Physics'
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221397631-d1f73fb3-9ebc-46ca-8853-91b06df180fe.png)

16. From the following table, write a SQL query to find the Nobel Prize winners in ‘Chemistry’ between the years 1965 and 1975. Begin and end values are included. Return year, subject, winner, and country.  

# TASK16

```sql
select year, subject, winner, country from nobel_win
where subject = 'Chemistry' and year >= 1965 and year <= 1975
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221397772-5603a7f3-1b10-464c-ac57-abb1294f041f.png)

17. Write a SQL query to display all details of the Prime Ministerial winners after 1972 of Menachem Begin and Yitzhak Rabin.

# TASK17

```sql
select * from nobel_win
where year > 1972 and winner in ('Menachem Begin', 'Yitzhak Rabin')
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221398176-ade39c12-cfe3-47eb-b7e7-3197959f2647.png)


18. From the following table, write a SQL query to retrieve the details of the winners whose first names match with the string ‘Louis’. Return year, subject, winner, country, and category. 


# TASK18

```sql
select * from nobel_win
where winner like 'Louis %'
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221398497-43459cf6-a33e-4c52-8fa3-6cf0d8b916b2.png)


19. From the following table, write a SQL query that combines the winners in Physics, 1970 and in Economics, 1971. Return year, subject, winner, country, and category.  


# TASK19

```sql
???
```

RESULT

20. From the following table, write a SQL query to find the Nobel Prize winners in 1970 excluding the subjects of Physiology and Economics. Return year, subject, winner, country, and category.  


# TASK20

```sql
select * from nobel_win 
where year = 1970 and subject not in ('Physiology', 'Economics')
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221399105-5167e322-9744-4d66-a4b7-6ab70a485441.png)


21. From the following table, write a SQL query to combine the winners in 'Physiology' before 1971 and winners in 'Peace' on or after 1974. Return year, subject, winner, country, and category.


# TASK21

```sql
???
```

RESULT


22. From the following table, write a SQL query to find the details of the Nobel Prize winner 'Johannes Georg Bednorz'. Return year, subject, winner, country, and category.  

# TASK22

```sselect * from nobel_win 
where winner = 'Johannes Georg Bednorz'
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221399292-bfd2d46a-b0fd-4b9b-b826-bf4e4ac5d555.png)


23. From the following table, write a SQL query to find Nobel Prize winners for the subject that does not begin with the letter 'P'. Return year, subject, winner, country, and category. Order the result by year, descending and winner in ascending. 

# TASK23

```sql
select * from nobel_win
where subject not like 'P%'
  order by year desc, winner
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221399780-3a71bae3-9f8d-4198-92e6-cc28969f3f56.png)


24. From the following table, write a SQL query to find the details of 1970 Nobel Prize winners. Order the results by subject, ascending except for 'Chemistry' and ‘Economics’ which will come at the end of the result set. Return year, subject, winner, country, and category.


# TASK24

```sql
???
```

RESULT


25. From the following table, write a SQL query to select a range of products whose price is in the range Rs.200 to Rs.600. Begin and end values are included. Return pro_id, pro_name, pro_price, and pro_com.  

# TASK25

```sql
select * from item_mast
where pro_price 
between 200 and 600
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221400046-1d791f82-619c-4cec-bc67-ca3814e85652.png)



# TAS26


# TASK27


# TASK28 


# TASK29

# TASK30

# TASK31

# TASK32

# TASK33
