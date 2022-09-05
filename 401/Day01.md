### What's the difference between PUT and PATCH?

ans => PUT and PATCH requests are HTTP verbs and both relate to updating the resources at a location.

the difference is: PUT is a method of modifying resources where the client sends data that updates the entire resource,

and replaces the entire resource if it exists or creates new if it does not exist.

PATCH does partial update e.g. Fields that need to be updated by the client, only that field is updated without modifying the other field.

### Provide links to 3 services or tools that allow you to "mock" an API for development like json-server

Mock APIs are used to simulate actual APIs where you can generate requests with custom data and get realistic responses the actual API would return.

ans => https://jestjs.io/docs/getting-started

https://www.cypress.io

https://www.postman.com

### Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?

ans => Swagger API call , 200 description 'ok', 400 bad request, 401 authorization information is missing or invalid, 404 user with this id is not found 500 to 599 unexpected error

### Compare and contrast SOAP and ReST

ans => As one REST API tutorial put it: SOAP is like an envelope while the REST is just postcard

SOAP – Simple Object Access Protocol – is probably the better known of the two models.

SOAP relies heavily on XML, and together with schemas, defines a very strongly typed messaging framework.

REST stands for Representational State Transfer. It is a software architecture style that relies on a stateless communications protocol, most commonly, HTTP. REST structures data in XML, YAML, or any other format that is machine-readable, but usually JSON is most widely used.

### Which 3 things had you heard about previously and now have better clarity on?

ans => patch and put

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

ans => REST API

### What are you most excited about trying to implement or see how it works?

ans => working on SOAP and REST API
