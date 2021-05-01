# CRUD: Create, Read, Update and Delete

In your own words, describe what each group of status code represents:
100’s = Codes that let you know the server is attemping to complete the request
200’s = Codes that let you know things are working
300’s = Codes that tell you that the requested info is in the same location
400’s = Codes that inform that the client has made an invalid request to a server
500’s = Codes that inform that the server is stressed or unreacheable

## What is a status code 202?

- A 202 informs the user that their request was recieved but that the return results will complete at a later time. 

## What is a status code 308?

- This means that a redirect has happened. It informs that the info is not located at the same location and that the URL has been moved.

## What code would you use if an update didn’t return data to a client?

- This would be code 200.

## What code would you use if a resource used to exist but no longer does?

- This would be a 404 code.

## What is the ‘Forbidden’ status code?

- This code means that the server uderstood the request but denied it.

## Why do we need to pull our MongoDB database string out of our server and put it into our .env? 

- We do this to attach the authentication key to it and so that our keys aren't displayed in our code for security reasons ie protecting the keys from malicious attackers.

## What is middleware?

- This is software that is available to operating systems that provide a service that the operating system can't do on its own.

## What does app.use(express.json()) do?

- This allows us to use the express dependency to access the .json data.
  
## What does the /:id mean in a route?

- It is the random number assigned by the db to keep track of the data stored in the db.
  
## What is the difference beween PUT and PATCH?

- The main difference between the PUT and PATCH method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource. 

*Resource from Wikipedia* [Wiki](/https://en.wikipedia.org/wiki/Patch_verb#:~:text=The%20main%20difference%20between%20the,instructions%20to%20modify%20the%20resource.)
  
## How do you make a defalut value in a schema?

- This is done automatically when a path is undefined within the schema.
  
## What does a 500 error status code mean?

- This means that the server could not complete the request due to an unexpected condition it could not resolve.

## What is the difference between a status 200 and a status 201?

- The 200 status code is by far the most common returned. It means, simply, that the request was received and understood and is being processed. A 201 status code indicates that a request was successful and as a result, a resource has been created (for example a new page).
- Resourced from [AloneOnAhill](/https://aloneonahill.com/blog/http-status-codes#:~:text=The%20200%20status%20code%20is,understood%20and%20is%20being%20processed.&text=A%20201%20status%20code%20indicates,for%20example%20a%20new%20page).

## Things I want to know more about...

This section is for writing questions and for listing things I might be curious about.

-----------------------------------------------------------
Content for this page are from online resources found under 301 Resources Class 13 at [Resources](/Resources.md)

[Back to Table of Contents](/README.md)