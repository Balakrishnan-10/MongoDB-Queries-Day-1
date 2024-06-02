# MongoDB: Non-Relational Database
* MongoDB is a document database with the scalability and flexibility that you want with the querying and indexing that you need.

## Queries:

1. Show all the Databases: ***Query: show dbs;***
2. Create a Database: ***Query:Use products;***

![Show dbs](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/ed9b9ba2-a61b-4ca2-98f9-b7c4582a2a4c)

3. Create a Collection and insert the Data: ***Query: db.products.insertMany();***

![Insert JSON Data](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/432dccac-00ef-4341-9248-4d53264d1a65)

# Find Queries:
### There are 2 methods to find and select data from a MongoDB collection, find() and findOne().

* Find all the information about each products ?
  
***Query: db.products.find().pretty();***

![Query 1](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/0696f483-dfeb-4689-a115-fa461a1b9c78)

* Find the product price which are between 400 to 800 ?

***Query: db.users.find({product_price:{$gte:400,$lt:800}});***

![Query 2](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/7c0ec7d5-8783-4274-a148-cdb82c9d2a3c)

* Find the product price which are not between 400 to 600 ?
  
***Query: db.users.find({product_price:{$not:{$gte:400,$lte:600}}});***

![Query 3](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/7a86ddc8-96c9-46be-9d69-0f1be4b052a3)

* List the four product which are greater than 500 in price ?
  
***Query: db.users.find({product_price:{$gte:500}}).limit(4);***

![Query 4](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/2e7b9132-beaa-44e3-b903-56bdb438266a)

* Find the product name and product material of each products ?
  
***Query: db.products.find({},{product_name:1,product_material:1});***

![Query 5](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/00a76a71-f95a-4672-8749-497c25db641b)

* Find the product with a row id of 10 ?
  
***Query: db.products.find({id: "10"});***
  
![Query 6](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/90a9cc21-3a39-4178-9d05-74c853037709)

* Find only the product name and product material ?
  
***Query: db.products.find({},{product_name:1,product_material:1,_id:0});***

![Query 7](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/04d7c57b-b5aa-46f7-baf5-b7f88a2b9249)

* Find all products which contain the value of soft in product material ?
  
***Query: db.products.find({"product_material": "soft"}); (OR) db.products.find({"product_material":{$eq:"soft"}});***

![Query 8](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/00bce282-9aea-4e78-a880-93b6d7369caf)

* Find products which contain product color indigo  and product price 492.00 ?
  
***Query: db.products.find({$or:[{product_color:"indigo"},{product_price:492.00}]});***

![Query 9](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/7e5ce467-78dd-4a86-acba-fb607fde7627)

# DELETE Query:
### The MongoDB shell provides the following methods to delete documents from a collection:
1.    To delete multiple documents, use db.collection.deleteMany().
2.    To delete a single document, use db.collection.deleteOne().

* Delete the products which product price value are 28 ?
  
***Query: db.products.deleteOne({product_price:28.00});***

  ![Query 10](https://github.com/Balakrishnan-10/MongoDB-Queries-Day-1/assets/157093363/955364a6-84ea-4921-a99f-4267de21e2ba)
