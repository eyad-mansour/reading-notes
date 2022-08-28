100’s =
usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client. Like using a different protocol or telling the client that its request will fail before they start sending the body.
200’s =
this doesn’t mean the request was successfully processed only that it met all validation requirements at the time of sending.
300’s =
tell the client that the resource they are requesting isn’t available at the expected location anymore. This can have multiple reasons, be temporary or permanent, but the client has to issue a request to the new location.
400’s =all about invalid requests a client sent to a server
500’s =they indicate problems with overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server.

Q-) What is a status code 202?

ans---) asynchronous processing of a request

Q-) What is a status code 308?

ans---) 308 Permanent Redirect - This tells the client to use another URL to access the resource and not use the current URL anymore.

Q-) What code would you use if an update didn’t return data to a client?

ans---) 204 No Content - A proper code for updates that don’t return data to the client

Q-) What code would you use if a resource used to exist but no longer does?

ans---) 414

Q-) What is the ‘Forbidden’ status code?

ans---) 403

Q-) Why do we need to pull our MongoDB database string out of our server and put it into our .env?

ans--) we will not use localhost we will use something else I mean he didnt really explain why but I think because it is sensitive data

Q-) What is middleware?

ans--) software that provides common services and capabilities to applications outside of what’s offered by the operating system

Q-) What does app.use(express.json()) do?

ans--) this line of code will make our server accept Json

Q-) What does the /:id mean in a route?

ans--) it is parameter and we can access using req

Q-) What is the difference between PUT and PATCH?

ans--) put will update all the information but patch will update the information that just getting passed

Q-) How do you make a default value in a schema?

ans--) default value if the server didnt pass the data that should pass

Q-) What does a 500 error status code mean?

ans--) there is error in the server

Q-) What is the difference between a status 200 and a status 201?

ans--) 201 mean object successfully created 200 is just mean successful not specific
