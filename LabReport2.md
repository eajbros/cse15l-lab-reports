# Lab Report 2
---
## Part One
## `StringServer.java` code
![*String Server Code*](StringServerSS.png)
---
## `/add-message` Example one
![*Add Hello World Server*](AddHelloWorld.png)
- Which methods in your code are called?
  > The method `handleRequest(URI url)` was called during this use of `/add-message` 

- What are the relevant arguments to those methods, and the values of any relevant fields of the class?
  > The argument to this method is `http://localhost:4000/add-message?s=Hello%20World`, and the values of the fields in this class are `""` for `str` and `0` for `requests`.

- How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
  > When this method sees the `/add-message` path, it increments the value of `requests` by one, making its new value `1`. This method also updates the value of `str` to the request number, the string inside the query, and a new line. This makes the new value for str `"1. Hello World \n"`.

---
## `/add-message` Example Two
![*Add Hello World Server*](AddXylophone.png)
- Which methods in your code are called?
  > The method `handleRequest(URI url)` was called during this use of `/add-message` 

- What are the relevant arguments to those methods, and the values of any relevant fields of the class?
  > The argument to this method is `http://localhost:4000/add-message?s=Xylophone`, and the values of the fields in this class are `"1. Hello World \n 2. I am Ethan \n 3. Third String"` for `str` and `3` for `requests`.

- How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
  > When this method sees the `/add-message` path, it increments the value of `requests` by one, making its new value `4`. This method also updates the value of `str` to add the request number, the string inside the query, and a new line. This makes the new value for str `"1. Hello World \n 2. I am Ethan \n 3. Third String \n 4. Xylophone"`.
---
## Part 2

