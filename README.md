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
