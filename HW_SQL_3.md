# telran-General-Technologies

Напишите запрос (в рамках "песочницы"), который покажет данные о заказах и клиентах, а именно:
ID заказа
имя клиента
страна назначения
название компании-перевозчика
```
SELECT
	Orders.OrderID,
    Customers.CustomerName,
    Customers.Country,
    Shippers.ShipperName
   
FROM [Orders]
JOIN Customers ON Orders.CustomerID=Customers.CustomerID
JOIN Shippers ON Orders.ShipperID=Shippers.ShipperID
```
