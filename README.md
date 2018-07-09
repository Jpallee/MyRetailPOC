# MyRetailPOC
A POC on RESTful webservice
# Description
myRetail is a rapidly growing company with HQ in Richmond, VA and over 200 stores across the east coast. myRetail wants to make its internal data available to any number of client devices, from myRetail.com to native mobile apps.

The goal for this exercise is to create an end-to-end Proof-of-Concept for a products API, which will aggregate product data from multiple sources and return it as JSON to the caller.

Here i am creating a RESTful service that can retrieve product name and price details by product id. 

### This application performs the following actions:
- Responds to an HTTP GET request at /products/{id} and delivers response as a JSON.
- Performs a HTTP GET request to retrieve the product name from an external API.
- Retrieves price information from Mongo data store and combines it with response JSON.
- Accepts a HTTP PUT request at /products/{id} and update the product’s price in the Mongo DB data store.


# Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.
## Prerequisites
Java 1.8

Mongo DB server

Eclipse IDE

## Built With
Spring Boot  2.0.3

Mongo DB 4.0

Maven

Mokito/Junit

## Installation
These softwares/tools to be installed to run this POC

1. Java 1.8
2. Eclipse Oxygen 
3. Mongo DB server - https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/
4. Postman 

Unzip the project, Import to eclipse as Exisitng Maven projects,select the project folder, check POM.xml and Click on Finish.

## Execution
Start mongo DB server. To start DB go to the Mongo Db installed path and execute mongod.exe from the command prompt.

Example: "C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe" --dbpath="c:\data\db"

After Importing the projecct into Eclipse, right click on the project and select Run As Spring Boot App.

Access the applictaion from Postmanwith below urls

GET Request : http://localhost:8080/products/52030896

PUT Request : http://localhost:8080/products/52030896 and provide below json in the body and select content type as JSON

{"id":13860428,"name":"The Big Lebowski (Blu-ray)","current_price":{"value":17.05,"currency_code":"USD"}}


## Tests
Junit test cases can be executed as Run As Junit test from eclipse.


## Author
Jayasree Palle
