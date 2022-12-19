# telran-General-Technologies

Напишите запрос, который покажет количественное распределение товаров по категориям (по убыванию):

```
SELECT CategoryID,
	COUNT (*) AS TOTAL_COUNT
    
FROM [Products]
	GROUP BY CategoryID
    ORDER BY TOTAL_COUNT DESC
```

Запрос, который изменит описание категории с ID = 3 на произвольное
```
UPDATE Categories
SET Description='.....'
WHERE CategoryID=3
```

Запрос, который покажет все товары с ценой от 100 до 150 (EURO)
```
SELECT *
FROM Products
WHERE Price BETWEEN 100 AND 150
```

Запрос - показать три самых дорогих товара
```
SELECT *
FROM Products
ORDER BY Price DESC
LIMIT 3
```

Запрос - удалить поставщиков с ID 1, 2, 4
```
DELETE FROM Suppliers
WHERE SupplierID IN (1, 2, 4)
```

Задача - добавить новую произвольную категорию товаров
```
INSERT INTO Categories
VALUES (10, '...', '...')
```

Запрос - который покажет товары с ценой в USD поля на выходе: (1) название товара (2) цена в USD (1 EURO == 1.05 USD)
```
SELECT ProductName,
	Price * 1.05 AS Price_USD
FROM Products
```
