# Angular2 With Spring Boot
Angular2 Typescript with Spring Boot

## Built With
[Spring Initializr](https://start.spring.io/) Spring Initializr bootstrap your application.
[Angular CLI](https://cli.angular.io/) A command line interface for Angular
## Installation
To run this app:
```sh
./gradlew bootRun
```
Test if app work at: [http://localhost:8080](http://localhost:8080)
## Tutorial 

1. create spring web project
3. generate angular2 frontend 
4. build angular2 frontend and copy to spring public folder
5. serve your web

#### 1 Create Spring Web project
You can use https://start.spring.io to init new project
Or you can use Spring CLI

```sh
spring init --build=gradle --dependencies=web angular2-with-springboot.zip
unzip  angular2-with-springboot.zip
cd  angular2-with-springboot
```
#### 2 Generate Angular 2 frontend 
We can use angular-cli to generate angular2 project
```sh
ng new angular2-frontend
```
#### 3 Build Angular2 Frontend and copy build folder to spring
```sh
cd angular2-frontend
ng build
```
The build artifacts will be stored in the dist/ directory.
We need to copy files in `dist` folder to spring public folder `src/main/resources/public`
```sh
cd ..
cp -r angular2-frontend/dist src/main/resources/public
```
#### 4 Serve your website
Now run your project
 ```sh
 ./gradlew bootRun
 ```
 and test if it work at [http://localhost:8080](http://localhost:8080)
