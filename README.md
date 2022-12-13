# telran-General-Technologies

Напишите запрос, который покажет количественное распределение товаров по категориям (по убыванию):

```
SELECT CategoryID,
	COUNT (*) AS TOTAL_COUNT
    
FROM [Products]
	GROUP BY CategoryID
    ORDER BY TOTAL_COUNT DESC
```
