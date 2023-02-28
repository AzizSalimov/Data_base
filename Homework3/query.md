1. Quyidagi jadvallardan har bir xodim uchun ism, familiya, bo‘lim raqami va bo‘lim nomini topish uchun SQL so‘rovini yozing.

# TASK1

```sql
select E.first_Name, E.last_name, E.department_id, D.department_name from employees E JOIN departments D On E.department_id = D.department_id
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/221772188-52e680d3-2257-496c-9a2b-86a8718f5abe.png)
