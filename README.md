sql
===
In order to learn SQL, we'll go through some simple exercises to start

Given the following statement:

CREATE TABLE `users` (
`id` int(11) unsigned NOT NULL AUTO_INCREMENT,
`email` varchar(255) NOT NULL,
`password` varchar(32) NOT NULL,
PRIMARY KEY (`id`)
);
What does the AUTO_INCREMENT flag do?
Increments the integer value.

What does int(11) mean?
Accept integer value of 11 digits and less only.

What is users in this statement?
The name of the table

Explain the concept of a primary key.

Explain the concept of a foreign key.

Queries

All the following questions deal with the attached SQL database. Make sure you follow the directions in the Google Doc on how to import the database.

Get a list of all the usernames from the users table.
SELECT * from USERS;


Get the name of all users who have placed orders for an iPhone.
select orders_products.order_id
from orders_products
  inner join products
		on orders_products.product_id = products.id
where products.name = 'iphone';
