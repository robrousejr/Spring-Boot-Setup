# Simple Springboot Application

## How to Setup

1. Download and install Maven, and Java 11 and properly set **JAVA_HOME** and insert Maven into the User Path (on Windows)
2. Go to [start.spring.io](https://start.spring.io/) and configure your project. I selected: 

   -  **Maven Project**
   - **Java**
   - **Jar**
   - **Java 11**
   - **Spring Boot DevTools** & **Spring Web**
   
This enabled me to create my web application.

3. Import into Eclipse as a **Maven Project**. 
4. Add **Auto Configuration** to ease my development.

*SimpleProjectApplication.java*
```
...
@SpringBootApplication
@RestController
@EnableAutoConfiguration
public class SimpleProjectApplication {
	@RequestMapping("/")
	String home() {
		return "Hello web";
	}

	public static void main(String[] args) {
		SpringApplication.run(SimpleProjectApplication.class, args);
	}
}

``` 

5. Run
   