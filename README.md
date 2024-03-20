#By combinding three files in Eclipse we can build an application


HTML Form (index.html):

The HTML form consists of two input fields where users can enter two numbers.
Upon submitting the form, the data is sent to the server-side servlet for processing.
The form action attribute is set to "add", indicating that the form data will be sent to a servlet mapped to the "/add" URL pattern.


Servlet Class (Test.java):

The servlet class, named Test, extends HttpServlet to handle HTTP requests.
It overrides the service method to process incoming requests.
Inside the service method, it retrieves the values of the parameters "num1" and "num2" from the request using req.getParameter().
It then parses these parameters into integers, performs addition, and stores the result in variable k.
Finally, it sends the result back to the client using the PrintWriter obtained from the HttpServletResponse.


Deployment Descriptor (web.xml):

The web.xml file serves as the deployment descriptor for the web application.
It defines a servlet named "abc" and maps it to the servlet class com.Kakarla.Test.
The servlet is mapped to the URL pattern "/add", meaning that any requests matching this pattern will be handled by the servlet.




#How to call Servlet from Servlet

HTML Form (index.html):

This file contains an HTML form with two input fields to enter two numbers.
When the form is submitted, it sends the entered values to the server.


TestServlet.java:

This Java class extends HttpServlet and handles the multiplication functionality.
It retrieves the two numbers entered by the user from the HTTP request.
Calculates the product of the two numbers.
Sets the calculated product as an attribute in the request.
Forwards the request to another servlet for further processing.


TestServlet_2.java:

This Java class extends HttpServlet and handles the squaring functionality.
It retrieves the calculated product from the request attribute.
Calculates the square of the product.
Writes the squared product as the response to the client.


web.xml:

This file is the deployment descriptor for the web application.
It configures the servlets (TestServlet and TestServlet_2) and their URL mappings.
Defines servlet-name, servlet-class, and URL patterns for each servlet.
Overall, this application demonstrates the basic usage of servlets to handle user input, 
perform calculations, and generate dynamic responses. The HTML form collects user input, which is then processed 
by servlets to perform mathematical operations, and the results are displayed back to the user.
