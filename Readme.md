
# Debezium example 
### MySQL to PG sequence example

- create test db and test table `users` with primary key in MySQL
- create test db in PG
- create connectors
- make some rows in Master test table
- Profit




## Creating connectors
curl -i -X POST -H "Accept:application/json" -H "Content-Type:application/json" http://localhost:8083/connectors/ -d @source.json
curl -i -X POST -H "Accept:application/json" -H "Content-Type:application/json" http://localhost:8083/connectors/ -d @sink.json


## Debezium connector manager  http://localhost:8080/
If you have any problem, then delete connector in install it again:  
- curl -i -X DELETE localhost:8083/connectors/p-s-connector  
- curl -i -X DELETE localhost:8083/connectors/m-s-connector


## Mysql Master test table
```
CREATE TABLE `test`.`users` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(100) NOT NULL DEFAULT 'vasya',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB;
```


#### Source list:
- https://programmerall.com/article/19392347675/


