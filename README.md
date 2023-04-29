# Домашнее задание к занятию "12.03 «SQL. Часть 1»" - Евгений Шахов.
---

### Задание 1.
##### Получите уникальные названия районов из таблицы с адресами, которые начинаются на “K” и заканчиваются на “a” и не содержат пробелов.
> select distinct addr.district from sakila.address addr where district like 'K%' and district like '%a' and district not like '% %';
> 
> ![image](https://user-images.githubusercontent.com/122415129/235296549-c34e1ece-516b-4c40-b531-bdaabf07f493.png)

---
### Задание 2.
##### Получите из таблицы платежей за прокат фильмов информацию по платежам, которые выполнялись в промежуток с 15 июня 2005 года по 18 июня 2005 года включительно и стоимость которых превышает 10.00.
> select * from sakila.payment where payment_date between '2005-06-15 00:00:00' and '2005-06-18 23:59:59' and amount >= 10 order by payment_date;
> 
> ![image](https://user-images.githubusercontent.com/122415129/235297183-a7ec367f-bed7-48d0-af1f-bf0ec10e4f5e.png)

---
### Задание 3.
##### Получите последние пять аренд фильмов.
> select * from sakila.rental order by rental_date desc limit 5;
> 
> ![image](https://user-images.githubusercontent.com/122415129/235297593-6062f870-acf7-4ca6-b2be-bf2c2b324997.png)

---
### Задание 4.
##### Одним запросом получите активных покупателей, имена которых Kelly или Willie. Сформируйте вывод в результат таким образом: все буквы в фамилии и имени из верхнего регистра переведите в нижний регистр, замените буквы 'll' в именах на 'pp'.
> select lcase(last_name) last_name, replace (lcase(first_name), 'll', 'pp') first_name, active from  customer where first_name = 'Kelly' or first_name = 'Willie'and active >0;
> 
> ![image](https://user-images.githubusercontent.com/122415129/235302727-c1071f7c-e85c-4797-b215-8ed0d0045c6b.png)


---
### Задание 5.
##### Выведите Email каждого покупателя, разделив значение Email на две отдельных колонки: в первой колонке должно быть значение, указанное до @, во второй — значение, указанное после @.
> 
> 

---
### Задание 6.
##### Доработайте запрос из предыдущего задания, скорректируйте значения в новых колонках: первая буква должна быть заглавной, остальные — строчными.
> 
> 

---
