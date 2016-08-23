# General Web Programming Questions

## Resources

- [What I Learned Doing 250 Interviews at Google](https://www.youtube.com/watch?v=r8RxkpUvxK0)
- [How to Prove Your Skills During an Interview](https://www.youtube.com/watch?v=i6mb4pZxNGM)

What is JSON?
> JavaScript Object Notation
> A minimal, readable data structure, mostly used to transmit data between a server and a web app. JSON is language independent.  

What is REST?
> REpresentational State Transfer
> An architecture style for designing networked applications. RESTful apps usually use HTTP requests to complete CRUD actions. REST is a lightweight and simple alternative to RPC (Remote Procedure Calls) and Web Services. REST is the software architectural style of the World Wide Web.
> In a well-designed RESTful app, a user navigates network of pages (a virtual state machine) by selecting links (state transitions) resulting in the next page (the next state of the app) being rendered.

What is HTTP?
> Hypertext Transfer Protocol
> HTTP is the foundation of data communication for the World Wide Web. An application layer protocol used by the WWW. HTTP is the protocol used between computers to transfer hypermedia documents, like HTML. Follows a classical client-server model. HTTP is a stateless protocol, meaning that the server does not keep any data between requests.

> From http://searchnetworking.techtarget.com/definition/TCP:
> "HTTP concepts include the idea that files can contain references to other files whose selection will elicit additional transfer requests. Any Web server machine contains, in addition to the Web page files it can serve, an HTTP daemon, a program that is designed to wait for HTTP requests and handle them when they arrive. Your Web browser is an HTTP client, sending requests to server machines. When the browser user enters file requests by either "opening" a Web file (typing in a Uniform Resource Locator or URL) or clicking on a hypertext link, the browser builds an HTTP request and sends it to the Internet Protocol address (IP address) indicated by the URL. The HTTP daemon in the destination server machine receives the request and sends back the requested file or files associated with the request. (A Web page often consists of more than one file.)"

What is TCP?
> Transmission Control Protocol
> Standard that defines how to establish and maintain a network conversation via which application programs can exchange data. TCP enables two hosts to establish a connection and exchange streams of data. TCP is meant to be error free, meaning it guarantees the delivery of data while maintaining data in the order in which it was sent.

> From http://searchnetworking.techtarget.com/definition/TCP:
> "For example, when a Web server sends an HTML file to a client, it uses the HTTP protocol to do so. The HTTP program layer asks the TCP layer to set up the connection and send the file.  The TCP stack divides the file into packets, numbers them and then forwards them individually to the IP layer for delivery. Although each packet in the transmission will have the same source and destination IP addresses, packets may be sent along multiple routes. The TCP program layer in the client computer waits until all of the packets have arrived, then acknowledges those it receives and asks for the retransmission on any it does not (based on missing packet numbers), then assembles them into a file and delivers the file to the receiving application."

What is an API?
> Application Programming Interface.
> The publicly exposed and programmable part of an application. An interface for applications to communicate and transfer data between one another.

Explain statelesness
> Each interaction must contain enough information for the interaction to be carried out. HTTP is a stateless protocol because the server is not required to retain any information about each user. Requests and interactions will not be associated with one another, unless there is a specific reason to do so (such as the presence of a session ID or a cookie)

Explain the anatomy of a HTTP request & response
> ## Request:
> Request line, headers, an empty line, and the message body.
> The request line contains a method verb (GET, HEAD, POST, PUT, DELETE, CONNECT, OPTIONS, TRACE), the request-URI and protocol version and ends with CRLF (denotes end of  a line)
> Header allow the client to pass additional information to the server
> SOURCE: http://www.tutorialspoint.com/http/http_requests.htm

> ## Response:
> Status line with protocol version and status code
> Headers, which pass additional information about the response
> The response body
> SOURCE: http://www.tutorialspoint.com/http/http_responses.htm

Explain browser caching
> A cache is a place to store assets that make the loading of resources more efficient. Every browser comes with an implementation of an HTTP cache. HTTP response headers provide the browser with instructions regarding when and for how long the response can be cached by the browser.

What are cookies? What role do they play in web apps?
> Cookies are small pieces of data sent from a web server and stored in a user's browser. Cookies allow browsers to remember stateful information (i.e. items in a shopping cart), or record user activity. Authentication cookies allow servers to know if a user is logged in.
> MORE INFO: http://stackoverflow.com/questions/17000835/token-authentication-vs-cookies

What are web tokens?
>_
> MORE INFO: http://stackoverflow.com/questions/17000835/token-authentication-vs-cookies

What is local storage?
>_

What is CORS?
>_

What are CSRF attacks? Give an example
>_



What is cross browser compatibility?
>_


In as much detail as possible, explain what happens when I type 'google.com' into my navbar and hit enter.
  > - Browser constructs an HTTP request
    - Browser makes a DNS lookup to find the IP
    - There's a TCP handshake with the server
    - The HTTP request is sent - bits go across the wire
    - A Google server receives the request, probably in a load balancer of some sort
    - Forwards it on until it eventually gets to a server that processes the homepage
    - Server generates an HTTP response and sends it back to the browser
    - Browser parses the HTTP response, turns HTML into DOM, then visually draws the page
    - For every image, script tag etc... it checks the browser cache and makes new HTTP requests for everything missing

When was the last time you used a design pattern and how did you apply it? Please explain in depth.
>_

What are the 3 worst defects of your favorite programming language?
> In JavaScript you might mention floating point errors, variables can be global by leaving out `var`, toCharCode doesn't handle UTF8 characters well

What is an ORM?
>Object Relationship Mapping, it connects data in your database with functionality in your models to create objects.

>An ORM (for object relational mapping) is a tool that lets you access and change data from a database using an object paradigm. Instead of writing raw SQL and talking to the database directly yourself, you use an ORM to produce the code needed to interact with the database. ActiveRecord serves this purpose for Rails.

What are the 3 data sources that the params hash is compiled from?
>path variables,request body, and query string.

What is a relational database and how does it differ from a non-relational database?  Give examples
>Relational databases are composed of various tables that are 'related' by associations made from among the table entries. Non-relational databases have no table schema, instead they have individual models within whichall associated data is contained. Any SQL database is relational, MongoDB is an example of a non-relational DB.

>A relational database is based on the relational model. It organizes data into tables of columns and rows. Each one of these rows will have its own key. It's because of these keys that we can link a row to another by using its key, or as its called "a foreign key". Relational databases use SQL to query and change the database

>Examples: PostgreSQL, MySQL.

>A non-relational db does not use the same table/key model as a relational one. These types of databases are made to scale and handle much large amounts of data. Rather than use tables/keys, they use their own special frameworks.

What is REST?
>REST is an architecture style for designing web applications that utilizes HTTP to communicate between machines. These types of applications use HTTP requests to do CRUD operations. REST is considered a lightweight alternative to other architecture styles.

What does `git bisect` do?
>Git Bisect employs binary search to discover when a bug (surfaced by a subcommand) was introduced.

>git bisect will utilize binary to search different states of your code with the goal of finding the change that created/introduced a bug.

How would you design a URL shortener similar to bit.ly?
>_

What are some advantages/disadvantages to testing your code?
>_

What tools would you use to test your code's functionality?
>_

What is the difference between a unit test and a functional/integration test?
>_

What is the purpose of a code style linting tool?
>_
