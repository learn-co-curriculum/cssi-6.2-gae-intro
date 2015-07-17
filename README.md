---
tags: cssi, gae, python, mvc
level: 2
languages: python
---

#Breaking Down Google App Engine

**Google App Engine** is a Platform as a Service (PaaS) offering that lets you build and run applications on Google’s infrastructure. You upload your files through the App Engine interface and your app gets hosted on Google's servers. App Engine connects the back-end and front-end for you.

Before we continue to make our own webapps, we need to speak very briefly about how anyone on the internet can access the code that you write at home.

### Clients and Servers
The internet is a network of computers that communicate with eachother using HTTP, which defines how data is deliverd. We won't cover HTTP too much during CSSI but you can read more about it [here](http://www.tutorialspoint.com/http/http_overview.htm).

The computers can either be clients, servers or often times both.

![Client and Server Diagram](https://mdn.mozillademos.org/files/4291/client-server.png)

The webapps you build will
* Get data from a client -  a request 
* Use a server to send data back -  a response. 

A server is a computer that waits (listens) for requests and sends back responses. Clients are usually individuals on their web browser, and their requests might be typing in a certain URL or submitting certain information.

### Requests
When building webapps on App Engine you will need to conside how your users will interact with your app.
There are two ways that a client (users) can make a request (send data): **GET** and **POST**
 + GET - data is stored within a URL
 + POST - data is submitted and temporarily stored

You will learn how to deal with both of these types of requests later today.


### MVC
In week 1, we learned front-end languages: HTML and CSS and a back-end language: Python. Webapps need a way to connect the front-end, the back-end and will often need a database.

The way that many people refer to the connections between everything a webapp might need is MVC or Model-View-Controller.

<img src="http://lh3.ggpht.com/aviadezra/SHj6gLRSkSI/AAAAAAAAALg/0xkCGOXuefc/image_thumb3.png?imgmax=800" width=300px>

+ **Models** (Back-end data - Datastore in App Engine)
  + Stores the data
+ **Views** (Front-end - HTML Template in App Engine)
  + The front end, this is what the user sees.
+ **Controller** (Back-end logic - our Python scripts in App Engine)
 + The  the code that is in charge of making the back end  communicate to the front end 

This MVC - model view controller - framework is the way that most modern web applications are organized.
Keeping the functionality of our application in these separate directories helps us stay organized as our apps become more and more complex.

### Routes and Handlers
**Routes and Handlers**
Setting up a route in the application controller:
+ Routes are set up to match the URL in the navigation bar of the browser.
+ Using `http://www.tinykittens.com/ as an example.`
 + When users go this URL with their browser they are triggering the '/' route
 + When they go to `http://www.tinykittens.com/about`  they are triggering the '/about’ route
 + When they go to  `http://www.tinykittens.com/adopt`   they are triggering the '/adopt' route

Now's your chance to combine your creative and technical skills to fully express yourself with code.
