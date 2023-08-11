1. Retrieve all customers:

```
SELECT * FROM Customers;
```

2. Retrieve available cars:

```
SELECT * FROM Cars WHERE is_available = TRUE;
```

3. Retrieve rentals for a specific customer:

```
SELECT Rentals.rental_id, Cars.make, Cars.model, Rentals.rental_start, Rentals.rental_end, Rentals.total_amount
FROM Rentals
JOIN Cars ON Rentals.car_id = Cars.car_id
WHERE Rentals.customer_id = [customer_id];
```

4.  Calculate the total revenue:

```
SELECT SUM(total_amount) AS total_revenue
FROM Rentals;
```

5. Retrieve customers who rented a specific car:

```
SELECT Customers.first_name, Customers.last_name, Rentals.rental_start, Rentals.rental_end
FROM Rentals
JOIN Customers ON Rentals.customer_id = Customers.customer_id
WHERE Rentals.car_id = [car_id];
```

6. Retrieve the most rented car:

```
SELECT Cars.make, Cars.model, COUNT(Rentals.rental_id) AS rental_count
FROM Cars
JOIN Rentals ON Cars.car_id = Rentals.car_id
GROUP BY Cars.make, Cars.model
ORDER BY rental_count DESC
LIMIT 1;
```
