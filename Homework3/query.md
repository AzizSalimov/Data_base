1. Quyidagi jadvallardan har bir xodim uchun ism, familiya, bo‘lim raqami va bo‘lim nomini topish uchun SQL so‘rovini yozing.

# TASK1

```sql
select E.first_Name, E.last_name, E.department_id, D.department_name from employees E JOIN departments D On E.department_id = D.department_id
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221772188-52e680d3-2257-496c-9a2b-86a8718f5abe.png)

2. Quyidagi jadvallardan har bir xodim uchun ism, familiya, bo‘lim, shahar va viloyatni topish uchun SQL so‘rovini yozing.

# TASK2

```sql
select E.first_name, E.last_name,
D.department_name, L.city, L.state_province
from employees E
join departments D
on E.department_id = D.department_id
join LOCATIONS l
on D.location_id = L.location_id
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221774709-711d7ba2-46f4-4b6a-9598-5335c5111795.png)


3. Quyidagi jadvaldan barcha xodimlar uchun ism, familiya, ish haqi va ish darajasini topish uchun SQL so'rovini yozing.

# TASK3

```sql
select E.first_name, E.last_name, E.salary, J.grade_level from employees E
  join job_grades J
  on E.salary between J.lowest_sal and J.highest_sal
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221788016-a1426fef-04c9-446d-bc3a-74d2849bb6ec.png)


4. Quyidagi jadvallardan bo'lim ID 80 yoki 40 da ishlaydigan barcha xodimlarni topish uchun SQL so'rovini yozing. Ism, familiya, bo'lim raqami va bo'lim nomini qaytaring.


# TASK4

```sql
select E.first_name , E.last_name, E.department_id ,  D.department_name from  employees E join departments D on E.department_id = D.department_id and E.department_id IN (80 , 40) order by E.last_name;
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221802854-cde130b1-e004-4cbf-9744-655688c03b0e.png)


5. Quyidagi jadvallardan ismi ‘z’ harfi bo‘lgan xodimlarni topish uchun SQL so‘rovini yozing. Ism, familiya, bo'lim, shahar va viloyatni qaytaring.

```sql
select E.first_name, E.last_name,
D.department_name, L.city, L.state_province
from employees E
join departments D
on E.department_id = D.department_id
join locations L
on D.location_id = L.location_id
where E.first_name like '%z%'
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221815562-d475d74e-847f-4852-a141-2586f283b3ca.png)
