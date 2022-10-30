# Introduction 


Gin is a web framework written in Go (Golang). 

Gin features a **martini-like API with must better performance** (up to 40 times faster thanks to **httprouter**). 


# Features 
- **Fast** because of **Radix tree based routing**, which leaves a small memory foot pring, has no relfection, and allows for **predictable** api performance. 
- **Middleware Support** allows HTTP requests to be handled **by a chain of middlewares** and the final action. For example: **Logger, Authorization, GZIP** and finally post a message in the DB. 
- **Crash-free** since Gin can **catch a panic occured during a HTTP request and recover it**. This way, your server will always be available. 
- **JSON validation** since Gin can **parse and valiadte** requests. 
- **Routes grouping** allows you to organize your toues better. 
- **Error management** such as collecetiong **all of the erros occured during a HTTP request**. 
- **Rendering built-in** through Gins easy to use API for **JSON, XML, and HTML rendering**. 
- **Extendable** since creating new middlewares is so easy. 


# References 
Gin Team. (2022). *Introduction*. Gin Web Framework. <https://gin-gonic.com/docs/introduction> 
