# REST API starter

This application satisfies the requirements of Part I, 1. of the LBG project specification.

## Installation

To initialise the project you will need to install several dependencies, open up a git bash terminal from the repo directory and run the command:

~~~ bash
$ npm install
~~~

## Running the application yeah

In order to run the application, from your git bash terminal run:

~~~ bash
$ npm start
API Listening on http://localhost:8080
~~~

## Stopping the application

In order to stop the application from the git bash terminal that is running the server press ``CTRL`` + ``C``

## Running on a different port

To start the application on an alternative port to the default (8080) from your git bash terminal run:

~~~ bash
$ PORT=9090 npm start
API Listening on http://localhost:9090
~~~

## Functionality

### Through the browser

In order to interact with this application through a browser navigate to http://localhost:8080/ or change the port number to the alternative that you have used.

### CREATE

To create the example product run the command:

~~~ bash
$ curl -s -X POST http://localhost:8080/product/create -H 'Content-type:application/json' -d '{"name":"example product", "description":"this is an example", "price":9.99}'
~~~

### READ (all)

To read all of the products run the command:

~~~ bash
$ curl -s -X GET http://localhost:8080/product/read
~~~

### READ (one)

To read one of the products run the command:

~~~ bash
$ curl -s -X GET http://localhost:8080/product/read/<id>
~~~

n.b: For these commands anything surrounded by angled braces <> needs to be replaced by you

### UPDATE

To update one of the products run the command:

~~~ bash
$ curl -s -X PUT http://localhost:8080/product/update/<id> -H 'Content-type:application/json'  -d '{"name":"updated product", "description":"its brand new", "price":99.99}'
~~~

n.b: For these commands anything surrounded by angled braces <> needs to be replaced by you

### DELETE

To delete one of the products run the command:

~~~ bash
$ curl -s -X DELETE http://localhost:8080/product/delete/<id>
~~~

n.b: For these commands anything surrounded by angled braces <> needs to be replaced by you

---

By Jason Persad.

---
# Testing

To run tests on this project you can use:
~~~ bash
npm test
~~~

## EXAMPLES

### unit tests...

~~~ javascript
{
    name: "lemon",
    description: "a yellow citrus fruit",
    price: 0.35

}
~~~

### integration

test the RESTful end-points

test the DELETE endpoint...

path: /product/delete/1

we expect 

status code: 204
status text: No content

### system testing
example is system integration testing

e.g. CREATE a lemon --> get a 201 response
     READ all of the products and verify that output is as expected
     ... get a 200 code, OK text and the lemon and details in the message body

or black box testing... use front end and verify behaviour in UI

### user acceptance testing

GIVEN a user can access UI
WHEN  when they enter valid prod ID in update area
AND they enter a desc
AND they enter a price
AND they click PUT button
THEN the updated product is visible on the page

#### asdasda sdasd asd asdasd
### THIS IS BIZZLE 44444444444444444444444 EX 2


