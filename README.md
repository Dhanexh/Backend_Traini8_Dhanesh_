
# **Training Center**

This is a Springboot Project for running the application, that manages a registry of government-funded training centers.


### **Project Structure**

```
Backend_Traini8_Dhanesh_
├── pom.xml
├── src
│   └── main
│       ├── java
│       │   └── com.dhanesh
│       │       └── backend_traini8_Dhanesh_
│       │           ├── controller
│       │           │   └── TrainingCenterController.java
│       │           ├── model
│       │           │   ├── TrainingCenter.java
│       │           │   └── Address.java
│       │           ├── repository
│       │           │   └── ITrainingCenterRepo.java
│       │           ├── service
│       │           │   └── TrainingCenterService.java
│       │           └── Traini8Application.java
│       └── resources
│           └── application.properties
```

### **Prerequesties**
* Java 11
* Maven 3

### **Setup**
1. Clone this repository: git clone <https://github.com/Dhanexh/Backend_Traini8_Dhanesh_.git>
2. Open a terminal in the project directory.
3. Run mvn clean install to build the project.


### **Configuration**
* Edit `application.properties` to configure your database connection details (e.g., URL, username, password).
* Ensure you have the appropriate database driver dependency included in `pom.xml`.


### **Runing the Application**
* Run mvn ``spring-boot:run`` to start the application.


### **API Endpoints**
- **Create Training Center (POST /api/v1/trainingcenter):**
  -  Accepts a JSON request body of type CreateTrainingCenterRequest.
  - Returns a JSON response body of type CreateTrainingCenterResponse containing the saved training center details upon success.
  - Returns an error response with a descriptive message on validation failure or other exceptions.
- **Get All Training Centers (GET /api/v1/trainingcenter):**
  - Returns a JSON response body containing a list of all training centers in the database.
  - Returns an empty list if no training centers exist.


### **Functionality:**
- The application validates user input for mandatory fields, size constraints, email format, and phone number format.
- It persists training center information to a database using JPA.
- It handles exceptions and returns appropriate error responses.


### **Optional Feature (Filtering):**
- This implementation does not include data filtering functionality in the `GET` endpoint. You can extend the `TrainingCenterService` to implement filtering based on specific criteria using JPA criteria queries or specifications.


### **Testing:**
- Unit tests and integration tests are not included in this example but are highly recommended for ensuring application robustness. 


### **Deployment:**
- You can package the application as a JAR file using `mvn package` and deploy it to any Java application server that supports Spring Boot.


### **Contribution:**
- Feel free to extend this project by adding additional features, improving error handling, or implementing data filtering.


### **Author:**
- [@Dhanesh](https://www.github.com/Dhanexh)

