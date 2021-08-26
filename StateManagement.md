# State Management Options
1)Client Side State Management.
<br>
2)Server Side State Management.

### 1) Client Side State Management
 It is a way in which the information which is being added by the user or the information about the interaction happened  between the user and the server is stored on the client's machine or in the page itself.
                
This management technique basically makes use of the following:
      
#### 1)View State :  <br>
View State can be used to maintain the State at a page level. The term "Page Level" means that the information is being stored for a specific page and until that specific page is<br> active (i.e. the page which is being currently viewed by the user). Once the user is re-directed or goes to some other page, the information stored in the View State gets<br> lost.
#### 2)Hidden Fields : <br>
ASP.NET provides a server control called "Hidden Field" which can be used to store a value at a page level, which is similar to a View State. <br> The value of the Hidden Field is sent along in the HTTP Form Collection along with the value of other controls.

####  3)Query String
A Query String is a string which is appended to the end of the Page URL. It is very simple to use and can be used to send data across pages. It stores information in a key - value pair. A "?" signature is used to append the key and value to the page URL.
<br>

####  4)Cookies

ASP.Net provides another way of state management, which is by using Cookies. Cookies are one of the best ways of storing information.<br> It is nothing but a text file which is stored on the client's machine.
 <br>
         When the user sends a request to the server, the server creates a cookie and attaches a header and sends it back to the user along with the response.The browser accepts the cookie and stores it at a specific location on the client's machine.
 

### 2) Server Side State Management

It is another way which ASP.NET provides to store the user's specific information or the state of the application on the server machine.<br> It completely makes use of server resources (the server's memory) to store information.
 
- Session State: Session is one of the most common way which is being used by developers to maintain the state of the application. The Session basically stores the values as a dictionary collection in key/value pairs. It completely utilizes server resources to store the data. It is a secure way of storing data, since the data will never be passed to the client.
   * In-proc
   * State Server
   * SQL Server
   
- Application State :If the information that we want to be accessed or stored globally throughout the application, even if multiple users access the site or application at the same time, then we can use an Application Object for such purposes.
It stores information as a Dictionary Collection in key - value pairs. This value is accessible across the pages of the application / website.
There are 3 events of the Application which are as follows
-Application_Start
-Application_Error
-Application_End

