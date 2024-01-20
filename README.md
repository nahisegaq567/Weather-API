This project uses the WeatherForecast template to create a simple weather API using C#. This template
includes support for Swagger, which generates useful documentation and help pages for web APIs in
general.

The WeatherForecast template produces a page that has a curl command to test the weather API, a URL 
to test the API, the response code, body, and headers, and a drop-down list box with media types and
an example value + schema for performing these functions.

The DB context uses EF Core, and is registered with a Dependency Injection. The DI injects the database 
context into the controller. From there, the controller is configured to respond to web API requests by 
scaffolding the controller, which marks it with a [ApiController] attribute. The scaffolding and the
attribute is what allows the controller to respond to web API requests.

To prevent the ToDoItem object from being exposed, and prevent over-posting, a secret field is used to 
provide DTO (Data Transfer Object). This configures the controller to use DTO from the created DTO 
model. This provides security for the code.
	
