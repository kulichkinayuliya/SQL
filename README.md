# 📝 SQL-запросы

---

## ✏️ Задание 1
### Условие: 
Пришлите в качества ответа список запросов, которые необходимо провести на этом [ресурсе](https://qastudio.notion.site/SQL-1459cf7d33c64a0a872e80459d3c9aec).

### ✔️ Решение:
1. select name, surname from staff where age>24 and city='Moscow';
2. select name, surname from staff order by (age);
3. select staff.age from staff join positions on staff.position_id=positions.id where position_name='qa_engineer';
4. select staff.name, staff.surname from staff join positions on staff.position_id=positions.id where position_name='frontend_dev' limit 20;
5. select computers.computer_name from computers join positions on computers.id = positions.computer_id join staff on positions.id=staff.position_id where name = 'anastasia' and surname = 'morozova';
6. select count(id) from staff where city='Moscow';
7. select staff.name, positions.salary from staff join positions on staff.position_id=positions.id;
8. select sum(positions.salary) from positions join staff on positions.id=staff.position_id where city='Moscow';
9. select staff.city, sum(positions.salary) from staff join positions on staff.position_id=positions.id group by city;
10. select distinct city from staff where name is not null;
11. select distinct city from staff where city like '%k%';
12. select position_name, salary from positions where salary between 1500 and 2200;
13. select staff.name, staff.surname, positions.position_name from staff right join positions on staff.position_id=positions.id;

---

## ✏️ Задание 2
### Условие: 
Имеется две таблицы:

1. Таблица users : Хранит в себе данные пользователя: его идентификатор, логин, имя и фамилию: user_id , login , name , surname
2. Таблица pets : Содержит в себе информацию о питомцах пользователя: Идентификатор пользователя (внешний ключ), идентификатор животного, вид животного, его кличку и породу: user_id, pet_id, type, nickname, breed
   
Напишите SQL-запрос, возвращающий фамилию и имя всех владельцев котов Абиссинской (Abyssinian) породы. Отсортировать по алфавиту.

### ✔️ Решение:
Select users.name, users.surname from users join pets on users.user_id=pets.user_id where breed = 'Abyssinian' order by name, surname;

---

## ✏️ Задание 3
### Условие Тест 1: 
![](https://github.com/kulichkinayuliya/SQL/blob/main/file/WINWORD_8VT72x7rGd.png)

### ✔️ Решение:


   
