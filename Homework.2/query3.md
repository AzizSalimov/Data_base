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
