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


```sql
select * from salesman 
where not city in ('Paris', 'Rome')
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221487575-238b74e9-0702-4d67-a951-3a3b38f3a1bf.png)

4. Quyidagi jadvaldan identifikatori 3007, 3008 yoki 3009 qiymatlaridan biriga tegishli bo'lgan barcha mijozlar tafsilotlarini olish uchun SQL so'rovini yozing. customer_id, cust_name, city, grade va salesman_idni qaytaring.

```sql
select * from customer 
where customer_id in (3007, 3008, 3009)
```

RESULT 

![изображение](https://user-images.githubusercontent.com/122611579/221488042-4aa92cc2-2ddd-4b04-a181-c17f1c1e807d.png)

