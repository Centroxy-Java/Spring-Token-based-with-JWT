# Spring-Token-based-with-JWT

Configure Spring Security for JWT. Expose REST POST API with mapping/authenticate using which User will get a valid JSON Web Token. And then, allow the user access to the API /hello only if it has a valid token 

![image](https://user-images.githubusercontent.com/43759116/124279571-4cb45a80-db65-11eb-8881-673aeeda71fd.png)

Spring Security and JWT Configuration
We will be configuring Spring Security and JWT to perform two operations:

Generating JWT: Expose a POST API with mapping /authenticate. On passing the correct username and password, it will generate a JSON Web Token (JWT).

Validating JWT: If a user tries to access the GET API with mapping /hello, it will allow access only if a request has a valid JSON Web Token (JWT).

Generating JWT
![image](https://user-images.githubusercontent.com/43759116/124279998-c8aea280-db65-11eb-909f-439368f6eaad.png)

![image](https://user-images.githubusercontent.com/43759116/124280046-d7955500-db65-11eb-9432-d28de89f7325.png)

Validating JWT
![image](https://user-images.githubusercontent.com/43759116/124280069-e0862680-db65-11eb-8641-5841d4eddc7f.png)


Generate a JSON Web Token
Create a POST request with URL localhost:8080/authenticate. The body should have a valid username and password. In our case, the username is javainuse and the password is password. 

![image](https://user-images.githubusercontent.com/43759116/124280250-15927900-db66-11eb-8503-23178dc479bc.png)


Validate the JSON Web Token
Try accessing the URL localhost:8080/hello using the above-generated token in the header as follows:
![image](https://user-images.githubusercontent.com/43759116/124280339-31961a80-db66-11eb-9d38-443169ae3033.png)
