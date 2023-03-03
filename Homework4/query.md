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

![изображение](https://user-images.githubusercontent.com/122611579/222696962-4a32ddcc-cf3c-41ba-8ae5-425460eb8dbf.png)


# Staffs

```sql
create table Staffs
(
    id         serial not null primary key,
    first_name varchar(20)  not null ,
    last_name varchar(20) not null ,
    city varchar(20) not null
);

insert into Staffs(first_name, last_name, city) values ('Umid', 'Rustamov', 'Tashkent');
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/222697596-6d5d8449-76c5-4899-8974-e054d5091348.png)


# TEACHERS


```sql
create table Teacher
(
    id serial  not null primary key ,
    first_name varchar(20),
    last_name varchar(20),
    birt_date varchar(13),
    phone varchar(16)
);

insert into Teacher(first_name, last_name, birt_date, phone)
values ('Kadirov', 'Sardor', '1997-03-25', '+99833-070-70-00');
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/222698287-94468cdd-c988-472b-a82f-e42efabd85d2.png)


# STUDENTS

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


![изображение](https://user-images.githubusercontent.com/122611579/222698914-ede627d8-1250-4606-bf15-bb52df2cbc6f.png)


# DIRECTIONS 

```sql 
create table Directions
(
    id serial not null primary key ,
    route_name varchar(25) not null ,
    route_price int not null
);

insert into Directions(route_name, route_price) VALUES ('Undergraduate', 1000);
```

RESULT

![изображение](https://user-images.githubusercontent.com/122611579/222700081-34342fa0-52d6-45f2-9127-1cf2f4707886.png)


# REGION

```sql
create table Regions(
    id serial not null primary key ,
    coutry varchar(20) not null ,
    city varchar(20) not null ,
    region varchar(20) not null
);



insert into Regions(coutry, city, region) VALUES ('Uzbekistan', 'Tashkent', 'Sergeli');
```


RESULT

![изображение](https://user-images.githubusercontent.com/122611579/222700358-7775f3b6-ca58-4114-a90b-82f1f50ed091.png)


