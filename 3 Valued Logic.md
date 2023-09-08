## Exercise:

##### Question: adjust the following query to display the null values as "No Address"

>SELECT address2 
FROM customers

###### Solution
```python
SELECT COALESCE(address2,'No Address')
FROM customers
```


##### Question: Fix the following query to apply proper 3VL

>SELECT *
FROM customers
WHERE COALESCE(address2, null) IS NOT null;

###### Solution
```python
SELECT *
FROM customers
WHERE address2 IS NOT NULL;
```


##### Question: Fix the following query to apply proper 3VL


>SELECT coalesce(lastName, 'Empty'), * from customers
where (age = null);

###### Solution
```python
SELECT COALESCE(lastName, 'Empty'), * FROM customer 
WHERE (age IS NULL);
```