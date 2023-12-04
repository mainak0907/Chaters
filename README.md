# FullStack-Chatify
Full Stack Chat Application with Group Chat Option  built with socket.io, Express JS,Mongo DB,  login & signup functionality using JWT and encryption using bcrypt . Deployed on Render.

# Documentation 
## Middlewares - 
In Node.js and Express.js, the .use() method is a key method used to add middleware to the application's request-handling pipeline. Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. They can perform various tasks, modify the request or response objects, and terminate the request-response cycle by sending a response to the client or passing control to the next middleware function.

The basic syntax of the .use() method in Express.js is as follows:
```
app.use([path,] callback [, callback, ...])
```
path (optional): Specifies a path or path pattern to which the middleware should be applied. If no path is specified, the middleware will be executed for all requests.

callback: The middleware function or functions to be executed. These functions typically take three arguments: req (request object), res (response object), and next (a function to pass control to the next middleware in the stack).

## Mongoose Schema and Models , References -
Schema:

A schema is a blueprint that defines the structure of the documents within a MongoDB collection. It specifies the fields, their types, and any additional options or constraints.
Mongoose schemas are typically created using the mongoose.Schema class. You define the fields, their types, and any additional options within this schema.
Schemas can include various data types such as String, Number, Date, ObjectId, Array, etc. They can also have additional options like default values, required fields, validators, etc.
Schemas provide a way to enforce a specific structure for the documents in a collection, ensuring that they adhere to a predefined format.

Model:

A model is a constructor function created from a Mongoose schema. It represents a collection in the MongoDB database and provides an interface for querying and manipulating documents within that collection.
Mongoose models are created using the mongoose.model method. This method takes two arguments: the name of the collection (as a string) and the schema to use for the documents in that collection.
Once a model is created, you can use it to perform various database operations such as creating, updating, deleting, and querying documents.


In Mongoose, a "reference" is a way to establish a relationship between documents in different collections. Instead of embedding one document within another, you store a reference to the other document's ObjectId. This is often used to represent one-to-many or many-to-many relationships between documents.

## express-async-handler

express-async-handler is a middleware for Express.js, a popular web application framework for Node.js. This middleware is designed to simplify error handling in route handlers that use asynchronous functions (such as those that involve database queries or external API calls). It helps avoid the need for explicitly wrapping each route handler in a try-catch block to handle asynchronous errors.

## populate() in Mongoose

In Mongoose, the .populate() method is used to replace specified paths in a document with document(s) from other collection(s). It allows you to reference documents in another collection and include their details in the result of a query.

<img width="506" alt="image" src="https://github.com/mainak0907/FullStack-Chatify/assets/88925745/91d25318-cf5b-4112-8ae9-c0d37e829e18">

## JSON Web Token
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

Header
Payload
Signature

Therefore, a JWT typically looks like the following.

xxxxx.yyyyy.zzzzz

1. The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.
2. The payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims.
3. To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.

### How do JSON Web Tokens work?
In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned. Since tokens are credentials, great care must be taken to prevent security issues. In general, you should not keep tokens longer than required.

You also should not store sensitive session data in browser storage due to lack of security.

Whenever the user wants to access a protected route or resource, the user agent should send the JWT, typically in the Authorization header using the Bearer schema. The content of the header should look like the following:

```
Authorization: Bearer <token>
```

This can be, in certain cases, a stateless authorization mechanism. The server's protected routes will check for a valid JWT in the Authorization header, and if it's present, the user will be allowed to access protected resources. If the JWT contains the necessary data, the need to query the database for certain operations may be reduced, though this may not always be the case.

## Socket.io

Socket.IO is a JavaScript library for real-time web applications. It enables bidirectional communication between clients (typically web browsers) and servers, facilitating the development of interactive and dynamic applications. Socket.IO builds on standard web technologies, like WebSockets, while providing additional features and fallback mechanisms for environments where WebSockets are not supported.

Event-Based Communication:

Socket.IO uses an event-driven model for communication. Both the server and clients can emit events and listen for events. Events can carry data, enabling the exchange of information between different parts of an application.

1. Server-side methods

<img width="511" alt="image" src="https://github.com/mainak0907/FullStack-Chatify/assets/88925745/e41982e3-6716-4661-acd3-c9c49e2a2192">
<img width="497" alt="image" src="https://github.com/mainak0907/FullStack-Chatify/assets/88925745/d3872218-3174-491e-b236-ecc6936236e2">
<img width="519" alt="image" src="https://github.com/mainak0907/FullStack-Chatify/assets/88925745/8c1f5df3-2cc4-43b6-a89c-84fd899c075e">
<img width="493" alt="image" src="https://github.com/mainak0907/FullStack-Chatify/assets/88925745/457b73b9-26f8-486f-8b53-c2224f01e256">

2. Client-side methods

<img width="501" alt="image" src="https://github.com/mainak0907/FullStack-Chatify/assets/88925745/77b8523c-b7ae-4fc0-b335-e4e5c674a618">
<img width="492" alt="image" src="https://github.com/mainak0907/FullStack-Chatify/assets/88925745/92513566-0347-482c-81d2-b49c9d95aa40">
<img width="490" alt="image" src="https://github.com/mainak0907/FullStack-Chatify/assets/88925745/a45b6bbf-3077-4f3b-8e9e-6aaf4571009b">


## bcrypt - Encryption 

bcrypt is a library commonly used for securely hashing passwords. It employs a password hashing algorithm that is intentionally slow and computationally expensive, making it resistant to brute-force and rainbow table attacks. bcrypt is specifically designed for securely hashing passwords and is a popular choice for password hashing in web development.





   
