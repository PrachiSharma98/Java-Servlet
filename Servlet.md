##Servlet:-

1. What is a Servlet?
Servlets are the Java programs that run on the Java-enabled web server or application server. They are used to handle the request obtained from the webserver, process the request, produce the response, then send a response back to the webserver. 

Properties of Servlets are as follows:

Servlets work on the server-side.
Servlets are capable of handling complex requests obtained from the webserver.
**********************************************************************************************************************************************************************

2. How Servlet works?
Execution of Servlets basically involves six basic steps: 

The clients send the request to the webserver.
The web server receives the request.
The web server passes the request to the corresponding servlet.
The servlet processes the request and generates the response in the form of output.
The servlet sends the response back to the webserver.
The web server sends the response back to the client and the client browser displays it on the screen.
**********************************************************************************************************************************************************************

3. Why do we need For Server-Side extensions?

The server-side extensions are nothing but the technologies that are used to create dynamic Web pages. Actually, to provide the facility of dynamic Web pages, Web pages need a container or Web server. To meet this requirement, independent Web server providers offer some proprietary solutions in the form of APIs(Application Programming Interface). 
These APIs allow us to build programs that can run with a Web server. In this case, Java Servlet is also one of the component APIs of Java Platform Enterprise Edition which sets standards for creating dynamic Web applications in Java. 
****************************************************************************************************************************************************************************

4.What is Servlet Container?
Servlet container, also known as Servlet engine is an integrated set of objects that provide a run time environment for Java Servlet components. 
In simple words, it is a system that manages Java Servlet components on top of the Web server to handle the Web client requests. 
******************************************************************************************************************************************************************
5. What is CGI?
The Servlet technology is similar to other Web server extensions such as Common Gateway Interface(CGI) scripts and Hypertext Preprocessor (PHP). However, Java Servlets are more acceptable since they solve the limitations of CGI such as low performance and low degree scalability.  

CGI is actually an external application that is written by using any of the programming languages like C or C++ and this is responsible for processing client requests and generating dynamic content. 
In CGI application, when a client makes a request to access dynamic Web pages, the Web server performs the following operations :  

It first locates the requested web page i.e the required CGI application using URL.
It then creates a new process to service the client’s request.
Invokes the CGI application within the process and passes the request information to the application.
Collects the response from the CGI application.
Destroys the process, prepares the HTTP response, and sends it to the client.
********************************************************************************************************************************************
6. JSP:-
It stands for Java Server Pages.
It is a server side technology.
It is used for creating web application.
It is used to create dynamic web content.
In this JSP tags are used to insert JAVA code into HTML pages.
It is an advanced version of Servlet Technology.
It is a Web based technology helps us to create dynamic and platform independent web pages.
In this, Java code can be inserted in HTML/ XML pages or both.
JSP is first converted into servlet by JSP container before processing the client’s request.
******************************************************************************************************************************************************
7.JSP pages are more advantageous than Servlet:
They are easy to maintain.
No recompilation or redeployment is required.
JSP has access to entire API of JAVA .
JSP are extended version of Servlet.
*******************************************************************************************************************************************************
8.Features of JSP
Coding in JSP is easy :- As it is just adding JAVA code to HTML/XML.
Reduction in the length of Code :- In JSP we use action tags, custom tags etc.
Connection to Database is easier :-It is easier to connect website to database and allows to read or write data easily to the database.
Make Interactive websites :- In this we can create dynamic web pages which helps user to interact in real time environment.
Portable, Powerful, flexible and easy to maintain :- as these are browser and server independent.
No Redeployment and No Re-Compilation :- It is dynamic, secure and platform independent so no need to re-compilation.
********************************************************************************************************************************************************
9.JSP Syntax:-

1.Declaration Tag :-It is used to declare variables.
Syntax:- 
<%!  Dec var  %>
Example:-
<%! int var=10; %>

2.Java Scriplets :- It allows us to add any number of JAVA code, variables and expressions.
 Syntax:- 
<% java code %>


3.JSP Expression :- It evaluates and convert the expression to a string.
 Syntax:- 
<%= expression %> 
 Example:- 
<% num1 = num1+num2 %> 



4.JAVA Comments :- It contains the text that is added for information which has to be ignored.
 Syntax:- 
<% -- JSP Comments %>
************************************************************************************************************************************

10.How is JSP Exceuted?

Steps for Execution of JSP are following:-
Create html page from where request will be sent to server eg try.html.
To handle to request of user next is to create .jsp file Eg. new.jsp
Create project folder structure.
Create XML file eg my.xml.
Create WAR file.
Start Tomcat
Run Application

*************************************************************************************************************************************************
11.Advantages of using JSP
It does not require advanced knowledge of JAVA
It is capable of handling exceptions
Easy to use and learn
It can tags which are easy to use and understand.


Disadvantages of using JSP
Difficult to debug for errors.
First time access leads to wastage of time
It’s output is HTML which lacks features.

***********************************************************************************************
12.JSP Life Cycle

Following steps are involved in the JSP life cycle: 
 

1.Translation of JSP page to Servlet:-This is the first step of the JSP life cycle. This translation phase deals with the Syntactic correctness of JSP. Here test.jsp file is translated to test.java. 
2.Compilation of JSP page(Compilation of JSP into test.java):-Here the generated java servlet file (test.java) is compiled to a class file (test.class). 
3.Classloading (test.java to test.class):-Servlet class which has been loaded from the JSP source is now loaded into the container. 
4.Instantiation(Object of the generated Servlet is created):-Here an instance of the class is generated. The container manages one or more instances by providing responses to requests. 
5.Initialization(jspInit() method is invoked by the container):-jspInit() method is called only once during the life cycle immediately after the generation of Servlet instance from JSP. 
6.Request processing(_jspService()is invoked by the container):-_jspService() method is used to serve the raised requests by JSP. It takes request and response objects as parameters. This method cannot be overridden. 
7.JSP Cleanup (jspDestroy() method is invoked by the container):-In order to remove the JSP from the use by the container or to destroy the method for servlets jspDestroy()method is used. This method is called once, if you need to perform any cleanup task like closing open files, releasing database connections jspDestroy() can be overridden. 

*****************************************************************************************************************************************
LifeCycle Of Servlet


Servlet Life Cycle Methods

There are three life cycle methods of a Servlet :

init()
service()
destroy()


Let’s look at each of these methods in details:

init() method: The Servlet.init() method is called by the Servlet container to indicate that this Servlet instance is instantiated successfully and is about to put into service.
//init() method

public class MyServlet implements Servlet{
   public void init(ServletConfig config) throws ServletException {
        //initialization code
   }
    //rest of code
}
service() method: The service() method of the Servlet is invoked to inform the Servlet about the client requests.
This method uses ServletRequest object to collect the data requested by the client.
This method uses ServletResponse object to generate the output content.
// service() method

public class MyServlet implements Servlet{
    public void service(ServletRequest res, ServletResponse res)
    throws ServletException, IOException {
            // request handling code
    }
    // rest of code
}
destroy() method: The destroy() method runs only once during the lifetime of a Servlet and signals the end of the Servlet instance.
//destroy() method

public void destroy()
As soon as the destroy() method is activated, the Servlet container releases the Servlet instance.

Servlet Life Cycle:
Servlet life cycle can be defined as the stages through which the servlet passes from its creation to its destruction.
The servlet life cycle consists these stages:

Servlet is borned
Servlet is initialized
Servlet is ready to service
Servlet is servicing
Servlet is not ready to service
Servlet is destroyed
Life cycle methods:
Life cycle methods are those methods which are used to control the life cycle of the servlet. These methods are called in specific order during the servlets’s entire life cycle.
The class Servlet provides the methods to control and supervise the life cycle of servlet. There are three life cycle methods in the Servlet interface. There are as follows:

init() method :
A servlet’s life begins here .
This method is called only once to load the servlet.Since it is called only once in it’s lifetime,therefore “connected architecture” code is written inside it because we only want once to get connected with the database.
Now Question Arises is that:-
Q.Why can’t we write connected architecture code inside the constructor, since constructor also run only once in it’s entire life?
Ans. Suppose if the connection doesn’t get established, then we can throw an exception from init() and the rest of the steps stop executing. But in the constructor we can’t use, throw in it’s prototype otherwise it is an error.
This method receives only one parameter, i.e ServletConfig object.
This method has the possibility to throw the ServletException.
Once the servlet is initialized, it is ready to handle the client request.
The prototype for the init() method:
public void init(ServletConfig con)throws ServletException{ }

where con is ServletConfig object



service() method :
The service() method is the most important method to perform that provides the connection between client and server.
The web server calls the service() method to handle requests coming from the client( web browsers) and to send response back to the client.
This method determines the type of Http request (GET, POST, PUT, DELETE, etc.) .
This method also calls various other methods such as doGet(), doPost(), doPut(), doDelete(), etc. as required.
This method accepts two parameters.
The prototype for this method:
public void service(ServletRequest req, ServletResponse resp) 
throws ServletException, IOException { }
where

req is the ServletRequest object which encapsulates the connection from client to server
resp is the ServletResponse object which encapsulates the connection from server back to the client

destroy() method :
The destroy() method is called only once.
It is called at the end of the life cycle of the servlet.
This method performs various tasks such as closing connection with the database, releasing memory allocated to the servlet, releasing resources that are allocated to the servlet and other cleanup activities.
When this method is called, the garbage collector comes into action.
The prototype for this method is:
public void destroy() { // Finalization code...}


***************************************************************************************************************************************************
The HttpSession Interface in Servlet:-


In web terminology, a session is simply the limited interval of time in which two systems communicate with each other. The two systems can share a client-server or a peer-to-peer relationship. However, in Http protocol, the state of the communication is not maintained. Hence, the web applications that work on http protocol use several different technologies that comprise Session Tracking, which means maintaining the state (data) of the user, in order to recognize him/her.

In order to achieve session tracking in servlets, cookies have been one of the most commonly used tech. However, they have the following disadvantages:

They can only keep textual information.
They’re browser dependent. Hence, if the client disables them, your web application can’t make use of them
Individual cookie can contain not more than 4kb of information.


Advantages of Http Sessions in Servlet

Any kind of object can be stored into a session, be it a text, database, dataset etc.
Usage of sessions is not dependent on the client’s browser.
Sessions are secure and transparent.

Disadvantages of Http session

Performance overhead due to session object being stored on server
Overhead due to serialization and de-serialization of data.


*******************************************************************************************************************************
Advantages of Http Sessions in Servlet

Any kind of object can be stored into a session, be it a text, database, dataset etc.
Usage of sessions is not dependent on the client’s browser.
Sessions are secure and transparent
Disadvantages of Http session

Performance overhead due to session object being stored on server
Overhead due to serialization and de-serialization of data.



Using HttpServletResponse Interface

The HttpServletResponse interface is entrusted with managing Http responses. To achieve servlet collaboration, it uses the following method:
public void sendRedirect(String URL)throws IOException;  
This method is used redirect response to another resource, which may be a servlet, jsp or an html file. The argument accepted by it, is a URL which can be both, absolute and relative. It works on the client side and uses the browser’s URL bar to make a request.
****************************************************************************************************************************************************

URL Rewriting using Java Servlet:-

Url rewriting is a process of appending or modifying any url structure while loading a page.

The request made by client is always a new request and the server can not identify whether the current request is send by a new client or the previous same client. Due to This property of HTTP protocol and Web Servers are called stateless. But many times we should know who is client in the processing request.
For example:
In any social networking site during login to till logout the server should know who is client so that server can manage all the request according to the user need.
This problem is solved by Session in Servlet.

Session : Session is a state between client and server and it contain multiple request and response between client and server. As we know that HTTP and Web Server both are stateless, the only way to maintain a session is when some unique information about the session (session id) is passed between server and client in every request and response.


Following are some ways by which we can provide unique id in request and response :

Session Interface in Servlet
Cookies Management
URL Rewriting


URL Rewriting

If your browser does not support cookies, URL rewriting provides you with another session tracking alternative. URL rewriting is a method in which the requested URL is modified to include a session ID. There are several ways to perform URL rewriting.
