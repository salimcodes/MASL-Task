![image](https://github.com/salimcodes/MASL-Tasks/assets/64667212/f6c5520e-52dc-4a4e-95dc-980e23a2a79d)

1. Create (INSERT)

```
-- Insert a new car
INSERT INTO Cars (make, model, year, mileage, rental_rate, is_available)
VALUES ('Toyota', 'Camry', 2022, 15000, 50.00, TRUE);
```

2. Read (SELECT)

```
-- Retrieve all cars
SELECT * FROM Cars;

-- Retrieve available cars
SELECT * FROM Cars WHERE is_available = TRUE;

-- Retrieve a specific car
SELECT * FROM Cars WHERE car_id = 1;
```

3. Update (UPDATE)

```
-- Update a car's rental rate
UPDATE Cars
SET rental_rate = 55.00
WHERE car_id = 1;
```

4. Delete (DELETE)

```
-- Delete a car
DELETE FROM Cars WHERE car_id = 1;
```
