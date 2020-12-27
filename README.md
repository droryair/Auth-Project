# Auth-Project

a simple back-end verification project, using JWT.  
this is a calculator, that only autheniticated users can use.  

________________________________________________________________


- :arrow_forward: how to run:  

- start the three servers in different terminals: user-server, auth-server, calc-server.  
- send two requests to the user-server:  
  -1.   
      - GET request to: http://localhost:3000/login , with body (JSON).  
      - the body needs to include: "userName" ,  "password".  
      - userName: "username1".  
      - password: "password1234".  
      - the app will check if the user exists, and if so- will print your token.  
      - copy the token you received.  
 -2.  
      - GET request to:   http://localhost:3000/calc , with body (JSON).  
      - the body needs to include: "token" , "number1" , "number2" , "action".  
      - token: paste from the previous sesponse.  
      - number1, number2: any numbers you want to calculate.    
      - action (optional): "add" / "sub" / "mult" / "div". default:"add"  
- the app wil check your token, and the existance of at least "number1" and "number2" , and will print the result.  
________________________________________________________________

### Examples using Postman:

First request:  
<kbd>  
<img src="https://github.com/droryair/Auth-Project/blob/master/assets/firstRequest.PNG" alt="First Request Example" height="400">   
</kbd>  
  
Second request:  
<kbd>  
<img src="https://github.com/droryair/Auth-Project/blob/master/assets/secondRequest.PNG" alt="Second Request Example" height="400">  
</kbd>

________________________________________________________________

### files in "keys" folder:  
-private.key  
-public.key  

________________________________________________________________

- :memo: to do:  
 - [ ] timeout for tokens
 - [ ] front-end