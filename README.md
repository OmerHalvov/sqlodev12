# sqlodev12
Patika SQL Ödev-12


Cevap-1:
SELECT COUNT(*) FROM film
WHERE length >
(
SELECT AVG(length) FROM film  
);

Cevap-2:
SELECT COUNT(*) FROM film
WHERE rental_rate =
(
SELECT MAX(rental_rate) FROM film  
);

Cevap-3:
SELECT title FROM film 
WHERE rental_rate = 
( 
 SELECT MIN(rental_rate)  FROM film 
) 
 AND replacement_cost = 
( 
SELECT  MIN(replacement_cost) FROM film  
)


Cevap-4:
SELECT customer_id ,COUNT(*) FROM payment
GROUP BY customer_id
ORDER BY COUNT DESC ;
