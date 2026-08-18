# Performance-Testing-Project-Using-Apache-JMeter.jmx
A performance testing project using Apache JMeter to evaluate web application performance, reliability, and scalability under varying user loads. It includes load and stress testing, virtual user simulation, and analysis of response time, throughput, error rate, and requests per second.


 Performance Testing Project Using Apache JMeter

 Project Overview

This project demonstrates API Performance Testing using Apache JMeter. The test plan is designed to evaluate the performance, responsiveness, reliability, and stability of a REST API under different workloads.

The JMeter test plan contains multiple API scenarios covering Product Management and Product Category operations**, including retrieving products, searching products, filtering and sorting products, and performing CRUD operations.

The main objective of this project is to understand how the API behaves under load and to identify potential performance bottlenecks.



 Tools & Technologies

Apache JMeter
REST API
HTTP/HTTPS
JSON
Git & GitHub
JMeter View Results Tree
JMeter Summary Report


 Project Structure

Performance-Testing-Project-Using-Apache-JMeter.jmx

	README.md
	Performance-Testing-Project-Using-Apache-JMeter.jmx


 API Test Scenarios

The JMeter test plan contains the following  requests:
Sl.no	Test Scenario	Description
1	Get All Products	Retrieves the complete list of available products.
2	Get a Single Product	Retrieves information for a specific product.
3	Search Products	Searches products based on a search parameter.
4	Limit and Skip Products	Tests product pagination using limit and skip parameters.
5	Sort Products	Retrieves products according to sorting criteria.
6	Get All Products Category	Retrieves available product categories.
7	Get All Products Category List	Retrieves the complete category list.
8	Get Products by a Category	Retrieves products belonging to a specific category.
9	Add a New Product	Tests product creation using a POST request.
10	Update a Product	Tests modification of an existing product.
11	Delete a Product	Tests deletion of an existing product.

API Operations Covered
The project covers the major REST API operations:
GET
Get All Products
Get Single Product
Search Products
Limit & Skip Products
Sort Products
Get All Product Categories
Gt all products category list
Get Products by a Category

POST
Add New Product

PUT
Update Product

DELETE
Delete Product




 Performance Testing Objectives

The main objectives of this project are:

 Measure API response time
 Analyze API throughput
 Measure error percentage
 Evaluate API stability under concurrent users
Identify slow-performing endpoints
 Verify API behavior under increased load
Analyze server response under different workloads
 Evaluate the scalability of the API


 Types of Performance Testing

This project can be used for different performance testing scenarios.

 1. Smoke Testing

A small number of users/requests are used to verify that the JMeter test plan and API endpoints are working correctly.

2. Load Testing

The application is tested with the expected number of concurrent users to evaluate normal workload performance.

3. Stress Testing

The number of concurrent users is gradually increased to determine the application's breaking point and behavior under heavy load.

 4. Spike Testing

A sudden increase in traffic is generated to observe how the API responds to unexpected workload spikes.
 5. Endurance Testing

The API can be executed for an extended period to identify memory leaks, performance degradation, or stability issues.



 JMeter Test Plan Components

The test plan can contain the following JMeter components:

Thread Group

Controls the number of virtual users, ramp-up time, and number of iterations.
Number of Threads: 5
Ramp-Up Period: 1 seconds
Loop Count: 5
The actual values should be adjusted according to the performance testing requirements.

 HTTP Request

Used to send REST API requests such as:
GET
POST
PUT
DELETE



Assertions

Used to validate API responses and determine whether requests are successful.



Response Code = 200


 Listeners

Used to analyze test execution and performance results.

Common listeners include:

View Results Tree
 Summary Report

The following metrics should be analyzed after test execution:

Metric	Description
Response Time	Time required by the API to respond to a request
Average Response Time	Average time taken by all requests
Min Response Time	Fastest recorded response time
Max Response Time	Slowest recorded response time
Throughput	Number of requests processed over a specific period
Error %	Percentage of requests that failed
90th Percentile	Response time below which 90% of requests completed
95th Percentile	Response time below which 95% of requests completed
99th Percentile	Response time below which 99% of requests completed

 How to Run the Project

 Step 1 — Install Java

 Install a compatible Java runtime required by your Apache JMeter version.

 Step 2 — Install Apache JMeter

 Download and extract Apache JMeter.

Open the JMeter `bin` directory.

 Step 3 — Open the JMX File

Open:


Performance-Testing-Project-Using-Apache-JMeter.jmx


in Apache JMeter.

Step 4 — Configure the Test

Configure:
Thread Group
	 Number of Threads
	Ramp-Up Period
	 Loop Count



Also verify the API host, port, path, request parameters, and request body where applicable.

 Step 5 — Run the Test

Start the test using the Startbutton in JMeter.

For performance execution, non-GUI/CLI execution is recommended for larger tests. Apache JMeter supports command-line execution for load tests.
bash

jmeter -n -t Performance-Testing-Project-Using-Apache-JMeter.jmx -l results.jtl




 Generate an HTML Performance Report
generate an HTML dashboard from the JMeter results:

bash
jmeter -g results.jtl -o reports


The generated report can then be opened from:

text
reports/index.html

Git Command:
git init

git add Performance-Testing-Project-Using-Apache-JMeter.jmx
git add README.md
git add Performance-Test-Report.html
git add .gitignore

git status

git commit -m "Add Apache JMeter performance testing project"

git branch -M main

git remote add origin https://github.com/khairuzzaman-nwu/Performance-Testing-Project-Using-Apache-JMeter.jmx.git

git push -u origin main





Test Execution Flow

text
Start
  ↓
Thread Group
  ↓
HTTP Request
  ↓
API Endpoint
  ↓
Response
  ↓
Assertion
  ↓
View Results Tree
  ↓
 Summary Report




 Expected Results

After execution, the performance report should help determine:

	Which API has the highest response time
	Which API has the lowest response time
	Overall API throughput
	Percentage of failed requests
	API behavior under concurrent users
	Performance degradation under heavy load
	Potential performance bottlenecks

Key Testing Areas

 
Sl.no	API Operation	HTTP Method	Endpoint
1	Get All Products	GET	https://dummyjson.com/products
2	Get a Single Product	GET	https://dummyjson.com/products/1
3	Search Products	GET	https://dummyjson.com/products/search?q=phone
4	Limit and Skip Products	GET	https://dummyjson.com/products?limit=10&skip=10&select=title,price
5	Sort Products	GET	https://dummyjson.com/products?sortBy=title&order=asc
6	Get All Product Categories	GET	https://dummyjson.com/products/categories
7	Get Product Category List	GET	https://dummyjson.com/products/category-list
8	Get Products by Category	GET	https://dummyjson.com/products/category/smartphones
9	Add a New Product	POST	https://dummyjson.com/products/add
10	Update a Product	PUT	https://dummyjson.com/products/1
11	Delete a Product	DELETE	https://dummyjson.com/products/1

API Testing Summary:
Method	Number of APIs	Purpose
GET	8	Retrieve and search product information
POST	1	Create a new product
PUT	1	Update an existing product
DELETE	1	Delete a product
Total	11	Complete Product API Test Suite


Endpoint paths should be updated if the API used in the JMeter project uses different routes.



 Skills Demonstrated

This project demonstrates practical knowledge of:

	Performance Testing
	API Testing
	REST API Testing
	Apache JMeter
	Load Testing
	Stress Testing
	API CRUD Testing
	HTTP Methods
	JSON Request/Response Handling
	Assertions
	Thread Groups

	View Results Tree
	Summary Report


The JMeter test plan covers the following API scenarios:

	Get All Products
	Get a Single Product
	 Search Products
	Limit and Skip Products
	Sort Products
	Get All Products Category
	Get All Products Category List
	Get Products by a Category
	Add a New Product
	Update a Product
	Delete a Product

 Project Screenshot:
 


API Performance Testing using Apache JMeter :
 Product API CRUD testing
Multiple GET API scenarios
POST, PUT and DELETE operations
Load testing capability
Response-time analysis
Throughput analysis
Error-rate analysis
View Results Tree
Summary Report

Contact 📞 For questions or feedback, please reach out:
Email: khairuzzaman173@gmail.com Github : https://github.com/khairuzzaman-nwu


