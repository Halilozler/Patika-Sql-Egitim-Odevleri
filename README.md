## 1.Ödev: <br/>
![Screenshot 2023-03-14 at 14 52 45](https://user-images.githubusercontent.com/45699509/224992852-03a7cf94-a496-4500-bda8-e9e1a62faeed.png) <br/>
1 -> SELECT tile, description FROM film   <br/>
2 -> SELECT * FROM film WHERE length > 60 AND length < 75 <br/>
3 -> SELECT * FROM film WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99) <br/>
4 -> SELECT last_name FROM customer WHERE first_name = 'Mary' <br/>
5 -> SELECT * FROM film WHERE NOT (length > 50 AND (rental_rate = 2.99 OR rental_rate = 4.99))  <br/>


## 2.Ödev: <br/>
![Screenshot 2023-03-14 at 15 03 41](https://user-images.githubusercontent.com/45699509/224995507-6a66eaea-b96f-4741-b990-2b05a2921254.png) <br/>
1 -> SELECT * FROM film WHERE replacement_cost BETWEEN 12.99 AND 16.99  <br/>
2 -> SELECT * FROM actor WHERE first_name IN('Penelope', 'Nick', 'Ed')   <br/>
3 -> SELECT * FROM film WHERE rental_rate IN(0,99, 2.99, 4.99) AND replacement_cost IN(12,99, 15.99, 28.99)   <br/>

## 3.Ödev: <br/>
![Screenshot 2023-03-14 at 15 22 13](https://user-images.githubusercontent.com/45699509/224999744-7a59b217-8514-4ddd-8f7c-1d51aedab550.png)  <br/>
1-> SELECT country FROM country WHERE LIKE 'A%a'  <br/>
2-> SELECT country FROM country WHERE LIKE '_____n'  <br/>
3-> SELECT title FROM film WHERE ILIKE '%t%t%t%t%'  <br/>
4-> SELECT title FROM film WHERE LIKE 'C%' AND length > 90 AND rental_rate = 2.99 <br/>

## 4.Ödev: <br/>
![Screenshot 2023-03-14 at 15 30 33](https://user-images.githubusercontent.com/45699509/225001591-c60a6b29-7102-4ae0-9845-3e0a3ab3dde0.png)  <br/>
1-> SELECT DISTINCT replacement_cost FROM film <br/>
2-> SELECT COUNT(DISTINCT replacement_cost) FROM film  <br/>
3-> SELECT * FROM film WHERE title LIKE 'T%' AND rating = 'G' <br/>
4-> SELECT COUNT(*) FROM country WHERE country_name LIKE '_____' <br/>
5-> SELECT COUNT(*) FROM city WHERE city_name ILIKE '%r' <br/>

<hr/>

## 5.Ödev: <br/>
![Screenshot 2023-03-14 at 15 54 41](https://user-images.githubusercontent.com/45699509/225007206-40970377-573f-45cd-91bc-a32e38d67522.png) <br/>
1-> SELECT * FROM film WHERE title LIKE 'n%' ORDER BY length DESC LIMIT 5 <br/>
2-> SELECT * FROM film WHERE title LIKE '%n' ORDER BY length ASC LIMIT 5 OFFSET 5 <br/>
3-> SELECT * FROM customer WHERE store_id = 1 ORDER BY last_name DESC LIMIT 4 <br/>

## 6.Ödev: <br/>
![Screenshot 2023-03-14 at 16 05 55](https://user-images.githubusercontent.com/45699509/225009997-fe7a4a2b-3111-429e-a964-0f0cc0f62ce6.png) <br/>
1-> SELECT AVG(rental_rate) FROM film <br/>
2-> SELECT COUNT(*) FROM film WHERE film_name LIKE 'C%'  <br/>
3-> SELECT MAX(length) FROM film WHERE rental_rate = 0.99  <br/>
4-> SELECT COUNT(DISTINCT replacement_cost) FROM film WHERE length = 150  <br/>

## 7.Ödev: <br/>
![Screenshot 2023-03-14 at 16 15 33](https://user-images.githubusercontent.com/45699509/225012681-c2ea62d6-d2fb-46d6-acab-8650cbe637c7.png) <br/>
1-> SELECT * FROM film GROUP BY rating <br/>
2-> SELECT * FROM film GROUP BY replacement_cost HAVING COUNT(*) > 50 <br/>
3-> SELECT COUNT(*) FROM customer GROUP BY store_id  <br/>
3-> SELECT country_id,COUNT(country_id) FROM city GROUP BY country_id ORDER BY COUNT(country_id) LIMIT 1 <br/>

## 8.Ödev: <br/>
![Screenshot 2023-03-14 at 16 37 06](https://user-images.githubusercontent.com/45699509/225018484-7e128ec3-311a-4049-af28-86fd8ac31711.png) <br/>
1-> CREATE TABLE employee( id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100)); <br/>
2-> INSERT INTO employee (id, name, birthday, email) values (1, 'Ronstring', '1981-07-19', 'zmayesk@skyrock.com'); <br/>
3-> UPDATE employee SET name = 'Silinecek' WHERE id > 1 <br/>
4-> DELETE FROM employee WHERE id BETWEEN 46 AND 50 <br/>

## 9.Ödev: <br/>
![Screenshot 2023-03-14 at 22 22 48](https://user-images.githubusercontent.com/45699509/225114864-5d528040-6e45-45f2-8f33-71570b31b30b.png) <br/>
1-> SELECT c.city_name, co.country_name FROM city c INNER JOIN country co ON c.Id = co.City_Id <br/>
2-> SELECT c.first_name, c.last_name, p.payment_id FROM customer c INNER JOIN payment p ON c.Id = co.Country_Id <br/>
3-> SELECT r.rental_id, c.first_name, c.last_name FROM customer c INNER JOIN rental r ON c.Id = r.Customer_Id <br/>

## 10.Ödev: <br/>
![Screenshot 2023-03-14 at 22 33 54](https://user-images.githubusercontent.com/45699509/225117140-246638cb-859d-4f36-89fb-f05edd40a27c.png) <br/>
1-> SELECT c.city_name, co.country_name FROM city c LEFT JOIN country co ON c.Id = co.City_Id <br/>
2-> SELECT c.first_name, c.last_name, p.payment_id FROM customer c RIGHT JOIN payment p ON c.Id = co.Country_Id <br/>
3-> SELECT r.rental_id, c.first_name, c.last_name FROM customer c FULL JOIN rental r ON c.Id = r.Customer_Id <br/>

## 11.Ödev: <br/>
![Screenshot 2023-03-14 at 22 39 37](https://user-images.githubusercontent.com/45699509/225118205-9590a49a-1892-4880-9524-b72096f756f5.png) <br/>
1-> ( SELECT first_name FROM actor ) UNION ( SELECT first_name FROM customer ) <br/>
2-> ( SELECT first_name FROM actor ) INTERSECT ( SELECT first_name FROM customer ) <br/>
3-> ( SELECT first_name FROM actor ) EXCEPT ( SELECT first_name FROM customer ) <br/>
4-> ( SELECT first_name FROM actor ) UNION ALL ( SELECT first_name FROM customer ) <br/>
4-> ( SELECT first_name FROM actor ) INTERSECT ALL ( SELECT first_name FROM customer ) <br/>
4-> ( SELECT first_name FROM actor ) EXCEPT ( SELECT first_name FROM customer ) <br/>

## 12.Ödev: <br/>
![Screenshot 2023-03-15 at 12 00 47](https://user-images.githubusercontent.com/45699509/225258987-d3ee0f55-40e0-46a7-889d-f9c40c6fecd9.png) <br/>
1-> SELECT COUNT(*) FROM film WHERE length > (SELECT AVG(length) FROM film) <br/>
2-> SELECT COUNT(*) FROM film WHERE rental_rate > (SELECT MAX(rental_rate) FROM film) <br/>
3-> SELECT * FROM film WHERE rental_rate = (SELECT MIN(rental_rate) FROM film) AND replacement_cost = (SELECT MIN(replacement_cost) FROM film)<br/>
4-> SELECT * FROM payment GROUP BY customer_id ORDER BY most_payments DESC <br/>
