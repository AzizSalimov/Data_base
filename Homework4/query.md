# DEPARTMENTS

```sql
create table Students
(
    id         serial      not null primary key,
    first_name varchar(45) not null,
    last_name  varchar(45) not null,
    phone      varchar(15) not null,
    email      varchar(50) not null
);


insert into Students(first_name, last_name, phone, email)
VALUES ('Javohir', 'Raxmatov', '+998905139545', 'javohirRaxmatov121@gmail.com');
```

RESULT

/home/aziz/Изображения/Снимки экрана/Снимок экрана от 2023-03-03 15-22-10.png
