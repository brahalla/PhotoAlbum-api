#PhotoAlbum

##About
This is an example RESTful API written in Java and Spring Framework. This project is intended to be a demo of how a REST API can be designed and how the project should be structured.

##Installation
To run this application you will first need to install a few packages (you can also install these packages with yum, brew, etc.)

JDK 1.7 - `sudo apt-get install openjdk-7-jre`
Maven - `sudo apt-get install maven`
PostgreSQL - `sudo apt-get install postgresql-9.4`

To build the PostgreSQL database when the API runs, set the following option in application.properties: `spring.datasource.initialize=false`

This project is built using Spring Boot, which makes it very easy to get running. You can either run the application directly from maven: `mvn spring-boot:run`, or you can build the application package with `mvn clean package` and then run the jar directly: `java -jar target/PhotoAlbum-1.0-SNAPSHOT.jar`.

##Usage
The endpoints for this application are `/api/photos` and `/api/albums`. To view all photos, you can navigate to:

```
http://localhost:8080/api/photos
```

Which should return the following:

```
[ {
  "id" : 1,
  "title" : "just me",
  "createdDate" : 1433203200000,
  "filePath" : "me.png",
  "albumId" : 1
}, {
  "id" : 2,
  "title" : "another pic",
  "createdDate" : 1433203200000,
  "filePath" : "another.png",
  "albumId" : 1
}, {
  "id" : 3,
  "title" : "profile photo",
  "createdDate" : 1433203200000,
  "filePath" : "profile.png",
  "albumId" : 1
}, {
  "id" : 4,
  "title" : "at the beach",
  "createdDate" : 1433203200000,
  "filePath" : "beach.png",
  "albumId" : 2
}, {
  "id" : 5,
  "title" : "at the park",
  "createdDate" : 1433203200000,
  "filePath" : "park.png",
  "albumId" : 2
} ]
```