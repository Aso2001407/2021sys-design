CREATE TABLE IF NOT EXISTS `d_purchase` ( 

  `order_id` bigint(20) NOT NULL AUTO_INCREMENT, 

  `customer_code` varchar(50) NOT NULL, 

  `purchase_date` date NOT NULL, 

  `total_price` int(11) NOT NULL, 

  PRIMARY KEY (`order_id`) 

) 
