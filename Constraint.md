# MySQL [ELZERO WEB SCHOOL]

##  Constraint القيود
Types of constraints:

1-Not Null 2- Null

```
ALTER TABLE students MODIFY username varchar(225) NOT NULL;
```

- #### Not Null

- #### Unique
لجعل الـ USERNAME غير متكرر في الجدول
```
ALTER TABLE students ADD UNIQUE (username);
```
لإلغاء خاصية ال unique
```
ALTER TABLE students DROP INDEX username;
```
```
ALERT TABLE students ADD test varchar(255) NOT NULL UNIQUE;
```
- #### PRIMARY KEY
خاصية الPRIMARY تنفع لصف واحد فقط
اضافة الPRIMARY KEY بطريقتين :

1-
```
CREATE TABLE classes (
  cid int NOT NULL PRIMARY KEY,
  name varchar(255) UNIQUE
);
```
2-
```
CREATE TABLE teacher (
  tid int NOT NULL,
  name varchar(255),
  PRIMARY KEY(tid)
);
```

```
CREATE TABLE teacher DROP PRIMARY KEY;
```
- #### FOREIGN KEY
```
CREATE TABLE clients (
  id int NOT NULL,
  email varchar(255) unique,
  PRIMARY KEY(id),
) ENGINE InnoDB;
```
```
CREATE TABLE orders (
  order_id int NOT NULL,
  price varchar(255) unique,
  client_id int NOT NULL,
  PRIMARY KEY(order_id),
  PRIMARY KEY(client_id),
);
```
