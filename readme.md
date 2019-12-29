to connect our source code into docker :

1. run docker machine
2. download node image from docker hub (Node by NodeJS )
3. run this command to run node image which is connected to your source code :
   docker run -p 8080:3000 -v D:/GitHub/ExpressSite:/var/www -w "/var/www" node npm start

   -p: ports

   8080: external port we can access to our app

   3000: internal port in our source code for express

   -v: set up a valume that points to our sourcecode in the current working directory.

   \* note that instead of D:/GitHub/ExpressSite that demonestrates where our source code hosted in our local machine in docker cli or mac we can use \${pwd} when we run this command in our project folder

   ***

   D:/GitHub/ExpressSite:/var/www: in container /var/www would point to our source code location

   -w: working directory and th path we write in " demonestrates our working directory

   npm start: actually it would forward the call from /var/www to our source code directory
