1. Quyidagi jadvaldan "Parij" yoki "Rim" shahridan kelgan sotuvchilarning tafsilotlarini topish uchun SQL so'rovini yozing. Sotuvchi_id, ism, shahar, komissiyani qaytaring.

# TASK1

```sql
select * from salesman 
where city = 'Paris' or city = 'Rome'
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221486112-26f6e039-8e3d-44ec-9ec0-7dfc5ab62dc2.png)


2. Quyidagi jadvaldan "Parij" yoki "Rim" dan kelgan sotuvchilar haqidagi ma'lumotlarni topish uchun SQL so'rovini yozing. Sotuvchi_id, ism, shahar, komissiyani qaytaring.

# TASK2

```sql
select * from salesman 
where city in ('Paris', 'Rome')
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221487191-d11413be-543e-4f6d-89d4-d14041ca897e.png)


3. Quyidagi jadvaldan Parij va Rimdan boshqa shaharlarda yashovchi sotuvchilar haqidagi ma'lumotlarni topish uchun SQL so'rovini yozing. Sotuvchi_id, ism, shahar, komissiyani qaytaring.

# TASK3

```sql
select * from salesman 
where not city in ('Paris', 'Rome')
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221487575-238b74e9-0702-4d67-a951-3a3b38f3a1bf.png)

4. Quyidagi jadvaldan identifikatori 3007, 3008 yoki 3009 qiymatlaridan biriga tegishli bo'lgan barcha mijozlar tafsilotlarini olish uchun SQL so'rovini yozing. customer_id, cust_name, city, grade va salesman_idni qaytaring.

# TASK4

```sql
select * from customer 
where customer_id in (3007, 3008, 3009)
```

RESULT 

![изображение](https://user-images.githubusercontent.com/122611579/221488042-4aa92cc2-2ddd-4b04-a181-c17f1c1e807d.png)


5. Quyidagi jadvaldan 0,12 dan 0,14 gacha komissiya oladigan sotuvchilarni topish uchun SQL so'rovini yozing (boshlang'ich va yakuniy qiymatlar kiritilgan). Sotuvchi_id, ism, shahar va komissiyani qaytaring.

# TASK5

```sql
select * from salesman 
where commission between 0.12 and 0.14
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221508208-a54f2d44-a535-441d-9bf1-70ab9d740341.png)

6. From the following table, write a SQL query to select orders between 500 and 4000 (begin and end values are included). Exclude orders amount 948.50 and 1983.43. Return ord_no, purch_amt, ord_date, customer_id, and salesman_id.

# TASK6

```
SELECT * FROM orders WHERE (purch_amt BETWEEN 500 AND 4000) AND NOT purch_amt IN(948.50,1983.43);
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221509026-038cc0b9-3639-4dd5-9dbd-f74813d5a19a.png)


7. Quyidagi jadvaldan ismlari "A" va "L" (shu jumladan emas) orasidagi har qanday harf bilan boshlanadigan sotuvchilarning tafsilotlarini olish uchun SQL so'rovini yozing. Sotuvchi_id, ism, shahar, komissiyani qaytaring.

# TASK7

```sql
SELECT *
FROM salesman
WHERE name BETWEEN 'A' and 'L';
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221509853-d59a3028-fa50-4deb-b473-7773f02a921e.png)


8. Quyidagi jadvaldan ismlari "A" va "L" (shu jumladan emas) orasidagi har qanday harf bilan boshlanadigan sotuvchilardan tashqari barcha sotuvchilarning tafsilotlarini topish uchun SQL so'rovini yozing. Sotuvchi_id, ism, shahar, komissiyani qaytaring.

# TASK8

```sql
SELECT *
FROM salesman
WHERE name NOT BETWEEN 'A' and 'L';
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221510331-b11bf790-3163-41c4-a52b-548b676dcce5.png)


9. Quyidagi jadvaldan ismlari 'B' harfi bilan boshlanadigan mijozlar tafsilotlarini olish uchun SQL so'rovini yozing. mijoz_identifikatori, maxsus_ism, shahar, daraja, sotuvchi_identifikatorini qaytaring.


# TASK9

```sql
SELECT *
FROM customer
WHERE cust_name LIKE 'B%';
```


RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221510504-34ed9849-1cf0-4448-b260-a28f3e68bd0a.png)


10. Quyidagi jadvaldan ismlari 'n' harfi bilan tugaydigan mijozlar tafsilotlarini topish uchun SQL so'rovini yozing. mijoz_identifikatori, maxsus_ism, shahar, daraja, sotuvchi_identifikatorini qaytaring.


# TASK10

```SQL
SELECT *
FROM customer
WHERE cust_name LIKE '%n';
```


RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221510676-611578b3-59e3-451f-9eaf-3a0a76fefcab.png)



11. Quyidagi jadvaldan ismlari ‘N’ va to‘rtinchi belgi ‘l’ bo‘lgan sotuvchilarning tafsilotlarini topish uchun SQL so‘rovini yozing. Dam olish har qanday belgi bo'lishi mumkin. Sotuvchi_id, ism, shahar, komissiyani qaytaring.

```SQL
SELECT *
FROM salesman
WHERE name LIKE 'N__l%';
```


RESULT 

![изображение](https://user-images.githubusercontent.com/122611579/221510821-00fdb2e8-9e5d-42cc-aa64-32ed2af5c123.png)


12. Quyidagi jadvaldan SQL so'rovini yozing, bunda col1 ning pastki chiziq ( _ ) dan chiqish belgisi bo'lgan qatorlarni toping. 1 qatorini qaytaring.


# TASK12

```SQL
SELECT *
FROM testtable
WHERE col1 LIKE '%/_%' ESCAPE '/';
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221511223-b9b9afb0-6322-4167-833e-6344d028aaec.png)


13. Quyidagi jadvaldan SQL so'rovini yozing, bu qatorlarda col1 da echib olish belgisi pastki chiziq ( _ ) bo'lmagan satrlarni aniqlang. 1 qatorini qaytaring.

```SQL
SELECT *
FROM testtable
WHERE col1 NOT LIKE '%/_%' ESCAPE '/';
```


RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221511338-72c5df71-e391-4da6-bd12-0d832eff45f9.png)
