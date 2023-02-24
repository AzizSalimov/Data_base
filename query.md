1.Categories jadval barcha ustun ma'lumotlarini bilan qaytaring

Task1

'''sql
'''

Result

![image](https://user-images.githubusercontent.com/122611579/221095800-9b7779ec-4167-4f3d-a4c0-9af892770204.png)


2.Categories jadval category_name va description ustun ma'lumotlarini qaytaring

Task2

select  category_name, description from categories

Result

![image](https://user-images.githubusercontent.com/122611579/221096205-a8321cac-232b-4561-9af2-4eeda05db162.png)


3. Categories jadval barchaa ustun ma'lumotlarini olishda ustun nomlarini o'zbekcha tarjimada qaytaring.

Task3

select toifalar_nomi.category_name as toifalar_nomi
from categories as toifalar_nomi

Result

![image](https://user-images.githubusercontent.com/122611579/221096319-4d52b9a2-7a68-4008-b803-8130eef30b1f.png)

4.Categories jadvaldan kategoriya nomi 'Confections'ga teng bo'lgan ma'lumotlarni qaytaring

Task4

select  category_name  from categories
where category_name = 'Confections'

Result

![image](https://user-images.githubusercontent.com/122611579/221096559-40282acf-6b3c-4a53-836a-8d3f255cee2c.png)


5. Categories jadvaldan kategoriya nomi 'Produce yoki 'Seafood', bo'lgan ma'lumotlarni qqaytaring.

Task5

select category_name from categories
where category_name = 'Produce' or category_name = 'Seafood'

Result

![image](https://user-images.githubusercontent.com/122611579/221096826-3606fed9-0e49-4e82-a070-c02c2a70c56a.png)



6. Categories jadvaldan quyida belgilangan ma’lumotlarni qaytaring.

Task6

select * from categories
where category_id between 6 and 8

Result

![изображение](https://user-images.githubusercontent.com/122611579/221102106-a283828d-15fa-4514-9d36-a494b3a8bfb1.png)


7. Categories jadvaldan ma'lumotlarni description alifbo bo'yicha Z-A tartibida chiqaring.

Task7

select * from categories
order by category_name desc


Result

![изображение](https://user-images.githubusercontent.com/122611579/221102163-5bbea35e-703c-4529-a166-60bb7ba1baf6.png)



8. Customers jadvalidan barcha ma'lumotlarni oling

Task8

SELECT * from customers

Result

![изображение](https://user-images.githubusercontent.com/122611579/221102209-c7da00eb-5eed-4454-a347-7869592d1f67.png)


9. Customers jadvalida ustun nomlarini o'zbekcha holatda oling

Task9

select customer_id as raqamlar,
       company_name as kompaniya_nomi,
       contact_name as kontakt_nomi,
       contact_title as kontakt_sarlavhasi,
       address as manzil,
       city as shahar,
       region as viloyat,
       postal_code as Pochta_kodi,
       country as mamlakat,
       phone as raqam,
       fax as faks

from customers;

Resilt

![изображение](https://user-images.githubusercontent.com/122611579/221102305-1af1c89d-6ba8-475f-86c1-2fdc2b6c17e9.png)


10.Customers jadvalidan contact_title 'Owner' bo'lgan ma'lumotlarni qaytaring

Task10

select * from customers
where contact_title = 'Owner'

Result

![изображение](https://user-images.githubusercontent.com/122611579/221103155-017c53c6-e541-4ba6-b439-b355d5b6750e.png)


11. Customers jadvalidan city 'London' bo'lgan ma'lumotlarni qaytaring

Task11

select * from customers
where city = 'London'


Result

![изображение](https://user-images.githubusercontent.com/122611579/221103249-431319ab-044b-4cae-9410-979a5b8cfe12.png)


12. Customers jadvalidan region ustun NULL bo'lgan ma'lumotlarni qaytaring

Task12

select customer_id ,company_name ,region from customers
where region is null

Result

![изображение](https://user-images.githubusercontent.com/122611579/221103313-6e085076-cc60-493c-adb7-94d484fd538d.png)


13. Customers jadvalidan region ustun NULL bo'lmagan ma'lumotlarni qaytaring

Task13

select customer_id, company_name, region from customers
where region is not null

Result

![изображение](https://user-images.githubusercontent.com/122611579/221103373-b837f0eb-0061-43fd-8518-47ab4a67c6a0.png)


14. Customers jadvalidan country ustun Germany bo'lgan ma'lumotlarni qaytaring

Task14

select * from customers
where country = 'Germany'


Result

![изображение](https://user-images.githubusercontent.com/122611579/221103480-cba7dd84-9037-4c79-b4a9-2ec14dd59ca4.png)


15. Customers jadvalidan country ustun Germany bo'lgan qatorlar sonini qaytaring
 
Task15

select count(*) from customers
where country = 'Germany'


Result

![изображение](https://user-images.githubusercontent.com/122611579/221103585-43a8e4b8-9ba1-4077-afbb-4d17c750750d.png)


16.Customers jadvalidan fax ustun NULL bo’lmalgan ma’lumotlarni contact_name ustun
alifbo tartiba tartiblab qaytaring

Task16

select * from customers
where fax is not null
    order by fax desc
    
Result

![изображение](https://user-images.githubusercontent.com/122611579/221103669-a90ffd9e-2b3a-4986-9b86-839dbf631a76.png)


17.Employees jadvaldan barcha ma’lumotlarni qaytaring.

Task17

select * from employees

Result

![изображение](https://user-images.githubusercontent.com/122611579/221103725-678f532f-c003-4319-b2cf-96811c677f8d.png)


18.Employees jadval ustun nomlarini o’zbekcha qaytaring.

Task18

select employee_id       as raqamlar,
       last_name         as familya,
       first_name        as ism,
       title             as sarlavha,
       title_of_courtesy as sarlavhasi,
       birth_date        as tugilgan_malumotlar,
       hire_date         as ijara_malumotlari,
       address           as manzil,
       city              as shahar,
       region            as mintaqa,
       postal_code       as Pochta_kodi,
       country           as mamlakat,
       home_phone        as uy_raqami,
       extension         as kengaytma,
       photo             as rasm,
       notes             as eslatmalar,
       reports_to        as murojat,
       photo_path        as fotosurat_yoli

from employees

Result

![изображение](https://user-images.githubusercontent.com/122611579/221103834-137683dc-c6e5-415c-96f6-a46098162c84.png)


19.Employess jadvaldan title_of_courtest ‘Mr’ bo’lgan xodimlarni firts_name alifbo tartibida
qaytaring

Task19

select * from employees
where title_of_courtesy = 'Mr.'
order by title_of_courtesy


Result

![изображение](https://user-images.githubusercontent.com/122611579/221103918-d0244da1-7970-472c-8d89-09b3f2a5b4cb.png)


20.Employes jadvalda title ‘Sales Representative’ bo’lgan xodimlar sonini qaytaring

Task20

select count(*) from employees
 where title = 'Sales Representative'
 
 
 Result
 
 ![изображение](https://user-images.githubusercontent.com/122611579/221103998-a02bd50b-1bfb-4bdd-88e7-c18e28199d0b.png)

 
 21.Employes jadvalda hire_date 1994-yilda bo’lgan ma’lumotlarni qaytaring.
 
 Task21
 
 select * from employees
where hire_date between '1994-01-01' and '1994-04-21';


Result
 
 ![изображение](https://user-images.githubusercontent.com/122611579/221104080-34eaebb3-b498-4ff1-9db9-2fe3e35542ed.png)

 
 22.Employes jadvaldan region NULL bo’lmagan xodimlarni first_name, last_name, title, city,
home_phone ma’lumotlarini first_name Z-A alifbo tartibida qaytaring.

Task22

select first_name , last_name , title,city, home_phone, city, title from employees
order by first_name desc;

Result

![изображение](https://user-images.githubusercontent.com/122611579/221104184-a3e27c92-8916-44ab-b3ee-e2f5e1f4897a.png)


23.Orders jadvaldan customer_id ‘VINET’ bo’lgan buyurtmalarni qaytaring.

Task23

select * from orders
where customer_id = 'VINET';

Result

![изображение](https://user-images.githubusercontent.com/122611579/221104240-457073e5-ed4d-4ab7-9d1e-4793b965a2a1.png)

 
 24.Orders jadvaldan order_date ustuni orqali 1996-yildagi ma’lumotlarni qaytaring.
 
 Task24
 
 select * from orders
where order_date between '1996-01-01' and '1996-11-24';

Result

![изображение](https://user-images.githubusercontent.com/122611579/221104345-6f074c66-2fa4-4695-822c-5c3393819ce4.png)
 
 
25.Orders jadvaldan ship_region ustun NULL bo’lmagan ma’lumotlarni qaytaring.

Task25

select * from orders
where ship_region is not null;

Result

![изображение](https://user-images.githubusercontent.com/122611579/221104429-543a410e-8a16-4eb0-8dc1-318944a6d88c.png)


26.Orders jadvaldan order_id 10300 va 10400 orasida bo’lgan ma’lumotlarni qaytaring.

Task26

select * from orders
where order_id between 10300 and 10400;

Result

![изображение](https://user-images.githubusercontent.com/122611579/221104461-32b8abb8-c254-4370-8bc5-43109c43aeef.png)


27.Order Details jadvaldan unit_price ustun umumiy qiymatini qaytaring.

Task27

select sum(unit_price) from order_details

Result

![изображение](https://user-images.githubusercontent.com/122611579/221104517-d51d1e64-c648-415e-9309-9a1f05386d43.png)





