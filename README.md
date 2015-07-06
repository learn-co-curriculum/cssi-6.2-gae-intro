---
tags: cssi, gae, python, mvc
level: 2
languages: python
---

#Google App Engine: Intro to Google App Engine

#Objectives:

+ Understand what App Engine is
+ Introduction of the Server Client and MVC models
+ Understanding the concept of front end vs. back end
+ What are HTTP response/requests
+ What are routes and handlers

#Motivation
You've seen how to use python to solve problems. You learned how to build out the front-end of a website. Now it's time to put those two essential components together. Once you've mastered App Engine, you'll have all the tools you need to build a fully functional, dynamic web application.

#Lesson:
Long ago, if you wanted to host a website on the internet, you would serve web pages from your own computer. If you were a company, this meant owning and maintaining big servers. If you were a hobbyist… it was hard!

Now, there are better ways to handle the infrastructure parts of serving your pages to your users. Google App Engine is a Platform as a Service (PaaS) offering that lets you build and run applications on Google’s infrastructure. Basically, you upload your code through the App Engine interface, then it lives on Google's machines and App Engine figures out the minutia of how to send the files to the right places.

App Engine Python Software Development Kit (SDK) gives you the nice launcher interface that you used, and it lets you simulate what will happen when your code is uploaded to Google's servers. That's what we did when we hit launch - started a mock server on our local machines that will do roughly the same thing as the real App Engine - serve a simple web page.

**Clients and Server**:
A server listens for HTTP requests from clients and sends back responses. Clients are usually individuals in their web browser, and their requests are usually asking for a web page at a particular url.

**So what is an HTTP request?**
+ The **Hypertext Transfer Protocol** (HTTP) is designed to enable communications between clients and servers.
+ HTTP works as a request-response protocol between a client and server.
+ A web browser may be the client, and an application on a computer that hosts a web site may be the server.
+ Example: A client (browser) submits an HTTP request to the server; then the server returns a response to the client. The response contains status information about the request and may also contain the requested content.

Two HTTP Request Methods: **GET** and **POST**
+ Two commonly used methods for a request-response between a client and server are: GET and POST.
 + GET - Requests data from a specified resource, usually a URL
 + POST - Submits data to be processed to a specified resource, the data is temporarily stored

<img src="http://lh3.ggpht.com/aviadezra/SHj6gLRSkSI/AAAAAAAAALg/0xkCGOXuefc/image_thumb3.png?imgmax=800" width=300px>

**MVC** stands for Model View Controller. It was conceived as a general solution to the problem of users controlling a large and complex data set. MVC is a way to organize our code in separate directories so that we can improve maintainability.
+ Models (Back-end - Datastore in App Engine)
  + The logic or code that goes into storing and maintaining the data in an application: Our models are written in python
  + The models are responsible for pulling data from database.
+ Views (Front-end - HTML Template in App Engine)
  + This directory is where we will store all of the HTML and CSS (and embedded Python) that gets displayed in the browser. This is what the user sees.
+ Controller (logic - our Python scripts in App Engine)
 + The application controller file in our project will hold all the code that is in charge of making the back end - the Python logic - communicate to the front end - the HTML in the browser that users interact with.

This MVC - model view controller - framework is the way that most modern web applications are organized.
Keeping the functionality of our application in these separate directories helps us stay organized as our apps become more and more complex.

**Routes and Handlers**
Setting up a route in the application controller:
+ Routes are set up to match the URL in the navigation bar of the browser.
+ Using http://www.tinykittens.com/ as an example.
 + When users go this URL with their browser they are triggering the '/' route
 + When they go to http://www.tinykittens.com/about  they are triggering the '/about’ route
 + When they go to  http://www.tinykittens.com/adopt   they are triggering the '/adopt' route

#Conclusion
Now's your chance to combine your creative and technical skills to fully express yourself with code. You have all the tools you need to make your own web application!
