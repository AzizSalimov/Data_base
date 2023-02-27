1. Quyidagi jadvaldan baho qiymati 100 dan yuqori bo'lgan mijozlar tafsilotlarini topish uchun SQL so'rovini yozing. customer_id, cust_name, shahar, baho va sotuvchi_identifikatorini qaytaring.

# TASK1

```sql
select * from customer
where grade > 100
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221405655-64fe50ad-1744-474e-9b88-1d7ceb5b24e6.png)


2. Quyidagi jadvaldan “Nyu-York” shahridagi bahosi 100 dan yuqori boʻlgan barcha mijozlarni topish uchun SQL soʻrovini yozing. customer_id, cust_name, city, grade va salesman_idni qaytaring.

# TASK2

```sql
select * from customer 
where city = 'New York' and grade > 100;
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221406052-9d1c9961-0f71-4b51-a692-053bc6c1c13f.png)


3. Quyidagi jadvaldan Nyu-York shahridan bo'lgan yoki bahosi 100 dan yuqori bo'lgan mijozlarni topish uchun SQL so'rovini yozing. customer_id, cust_name, city, grade va salesman_idni qaytaring.

# TASK3

```sql
select * from customer
where city = 'New York' or grade > 100
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221408464-e6f59cdc-5947-47b9-a89a-7a9eda7c773c.png)

4. Quyidagi jadvaldan "Nyu-York" shahridan bo'lgan yoki 100 dan yuqori bahoga ega bo'lmagan mijozlarni topish uchun SQL so'rovini yozing. customer_id, cust_name, city, grade va salesman_idni qaytaring.

# TASK4

```sql
select * from customer
where city = 'New York' or not grade > 100
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221409222-ee868e19-9e9d-4e81-8d67-872bf4fc323e.png)

5. Quyidagi jadvaldan "Nyu-York" shahriga tegishli bo'lmagan yoki bahosi 100 dan ortiq bo'lgan mijozlarni aniqlash uchun SQL so'rovini yozing. customer_id, cust_name, city, grade va salesman_idni qaytaring.


# TASK5

```sql
select * from customer 
where not (city = 'New York' or grade > 100)
```

RESULT


![изображение](https://user-images.githubusercontent.com/122611579/221471425-d41f6475-c175-4a4d-88fa-c8146899187a.png)


6. Quyidagi jadvaldan ord_date '2012-09-10'ga teng bo'lgan va sotuvchi_id 5005 dan yuqori yoki purch_amt dan katta bo'lganlar bundan mustasno barcha buyurtmalar tafsilotlarini topish uchun SQL so'rovini yozing. sotuvchi_identifikatori.


# TASK6

```sql
select * from orders 
where ((ord_date = '2012-09-10' or salesman_id > 5005) or purch_amt > 1000.00)
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221486796-588b69ed-8053-4aed-8dbc-e32ff2d70e49.png)



7. Quyidagi jadvaldan komissiyalari 0,10 dan 0,12 gacha bo'lgan sotuvchilarning tafsilotlarini topish uchun SQL so'rovini yozing. Sotuvchi_id, ism, shahar va komissiyani qaytaring.

# TASK7

```sql
select salesman_id, name, city, commission from salesman
where commission > 0.10 and commission < 0.12
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221475252-245b2f60-dc97-48d9-8cbe-04735d873d8d.png)


8. Quyidagi jadvaldan xarid summasi 200 dan kam bo‘lgan barcha buyurtmalar tafsilotlarini topish uchun SQL so‘rovini yozing yoki buyurtma sanasi “2012-02-10” dan katta yoki unga teng va mijoz identifikatori 3009 dan kam bo‘lgan buyurtmalarni istisno qiling. Ord_no, purch_amt, ord_date, customer_id va sotuvchi_identifikatorini qaytaring.

# TASK8

```sql
select * from orders 
where (purch_amt < 200 or not (ord_date >= '2012-02-10' and customer_id < 3009))
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221477185-3fe70e8d-2ae1-467f-a169-05ca3844d863.png)

9. Quyidagi jadvaldan quyidagi shartlarga javob beradigan barcha buyurtmalarni topish uchun SQL so'rovini yozing. Buyurtma sanasi “2012-08-17” yoki mijoz identifikatori 3005 dan katta va xarid summasi 1000 dan kam bo‘lgan kombinatsiyalar bundan mustasno.

# TASK9

```sql
select * from orders 
where not ((ord_date = '2012-08-17' or customer_id > 3005) and purch_amt < 1000);
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221480113-a28ac0e6-c2bb-4879-962b-bc9ae60819bf.png)


10. 6000 maqsadli qiymatining 50% dan oshgan buyurtmalar uchun buyurtma raqami, xarid miqdori va erishilgan va bajarilmagan foizlarni (%) ko'rsatadigan SQL so'rovini yozing.

# TASK10

```sql
???
```

RESULT


11. Quyidagi jadvaldan "Dosni" yoki "Mardy" familiyasi bo'lgan barcha xodimlarning ma'lumotlarini topish uchun SQL so'rovini yozing. emp_idno, emp_fname, emp_lname va emp_dept ni qaytaring.

# TASK11

```sql
select * from emp_details 
where emp_lname = 'Dosni' or emp_lname = 'Mardy'
```

RESULT 

![изображение](https://user-images.githubusercontent.com/122611579/221480837-e8bbd31c-aaf1-4df8-bcd2-694b8c0183fc.png)


12. Quyidagi jadvaldan 47 yoki 63-bo'limda ishlaydigan xodimlarni topish uchun SQL so'rovini yozing. Emp_idno, emp_fname, emp_lname va emp_deptni qaytaring.

 # TASK12
 
 ```sql
select * from emp_details 
where emp_dept = 47 or emp_dept = 63
 ```
 
 RESULT 
 
 ![изображение](https://user-images.githubusercontent.com/122611579/221481292-c8a22bff-c1fd-47f0-91a0-0bb8ae83e543.png)
