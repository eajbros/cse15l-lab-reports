# Lab Report 2
---
## `StringServer.java` code
![*String Server Code*](StringServerSS.png)
---
## /add-message
![*Add Hello World Server*](AddHelloWorld.png)
- Which methods in your code are called?
  > The method `handleRequest(URI url)` was called during this use of `/add-message` 

- What are the relevant arguments to those methods, and the values of any relevant fields of the class?
  > The argument to this method is `http://localhost:4000/add-message?s=Hello%20World`, and the values of the fields in this class are "" for `str` and 0 for `requests`.

- How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
  > 
