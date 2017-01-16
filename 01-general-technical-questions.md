# General Web Programming Questions

#### Resources

- [What I Learned Doing 250 Interviews at Google](https://www.youtube.com/watch?v=r8RxkpUvxK0)

What is JSON?
> JavaScript Object Notation
>
> A minimal, readable data structure, mostly used to transmit data between a server and a web app. JSON is language independent.  

What is REST?
> REpresentational State Transfer
>
> An architecture style for designing networked applications. RESTful apps usually use HTTP requests to complete CRUD actions. REST is a lightweight and simple alternative to RPC (Remote Procedure Calls) and Web Services. REST is the software architectural style of the World Wide Web.
> In a well-designed RESTful app, a user navigates network of pages (a virtual state machine) by selecting links (state transitions) resulting in the next page (the next state of the app) being rendered.

What is HTTP?
> Hypertext Transfer Protocol
>
> HTTP is the foundation of data communication for the World Wide Web. An application layer protocol used by the WWW. HTTP is the protocol used between computers to transfer hypermedia documents, like HTML. Follows a classical client-server model. HTTP is a stateless protocol, meaning that the server does not keep any data between requests.

> "HTTP concepts include the idea that files can contain references to other files whose selection will elicit additional transfer requests. Any Web server machine contains, in addition to the Web page files it can serve, an HTTP daemon, a program that is designed to wait for HTTP requests and handle them when they arrive. Your Web browser is an HTTP client, sending requests to server machines. When the browser user enters file requests by either "opening" a Web file (typing in a Uniform Resource Locator or URL) or clicking on a hypertext link, the browser builds an HTTP request and sends it to the Internet Protocol address (IP address) indicated by the URL. The HTTP daemon in the destination server machine receives the request and sends back the requested file or files associated with the request. (A Web page often consists of more than one file.)" ([Source](http://searchwindevelopment.techtarget.com/definition/HTTP))

What is TCP?
> Transmission Control Protocol
>
> Standard that defines how to establish and maintain a network conversation via which application programs can exchange data. TCP enables two hosts to establish a connection and exchange streams of data. TCP is meant to be error free, meaning it guarantees the delivery of data while maintaining data in the order in which it was sent.

> "For example, when a Web server sends an HTML file to a client, it uses the HTTP protocol to do so. The HTTP program layer asks the TCP layer to set up the connection and send the file.  The TCP stack divides the file into packets, numbers them and then forwards them individually to the IP layer for delivery. Although each packet in the transmission will have the same source and destination IP addresses, packets may be sent along multiple routes. The TCP program layer in the client computer waits until all of the packets have arrived, then acknowledges those it receives and asks for the retransmission on any it does not (based on missing packet numbers), then assembles them into a file and delivers the file to the receiving application." ([Source](http://searchnetworking.techtarget.com/definition/TCP))

What is an API?
> Application Programming Interface.
>
> The publicly exposed and programmable part of an application. An interface for applications to communicate and transfer data between one another.

Explain statelesness
> Each interaction must contain enough information for the interaction to be carried out. HTTP is a stateless protocol because the server is not required to retain any information about each user. Requests and interactions will not be associated with one another, unless there is a specific reason to do so (such as the presence of a session ID or a cookie)

Explain the anatomy of a HTTP request & response
> #### Request:
> Request line, headers, an empty line, and the message body.
>
> The request line contains a method verb (GET, HEAD, POST, PUT, DELETE, CONNECT, OPTIONS, TRACE), the request-URI and protocol version and ends with CRLF (denotes end of  a line)
>
> Header allow the client to pass additional information to the server
>
> SOURCE: http://www.tutorialspoint.com/http/http_requests.htm

> #### Response:
> Status line with protocol version and status code
>
> Headers, which pass additional information about the response
>
> The response body
>
> SOURCE: http://www.tutorialspoint.com/http/http_responses.htm

Explain browser caching
> A cache is a place to store assets that make the loading of resources more efficient. Every browser comes with an implementation of an HTTP cache. HTTP response headers provide the browser with instructions regarding when and for how long the response can be cached by the browser.

What are cookies? What role do they play in web apps?
> Cookies are small pieces of data sent from a web server and stored in a user's browser. Cookies allow browsers to remember stateful information (i.e. items in a shopping cart), or record user activity. Authentication cookies allow servers to know if a user is logged in.
> MORE INFO: http://stackoverflow.com/questions/17000835/token-authentication-vs-cookies

What are web tokens?
> Web tokens are small pieces of data stored on the client side. They are generated by the server when a user is successfully authenticated. They are usually signed for a certain period of time, after which they expire. Tokens are then sent with every request. The server checks that the token is valid, and uses this information to serve specific assets to the user. Tokens can be used to authenticate users across third party applications, because they only contain only the specific information needed for each application. Tokens are usually stored in local storage> They may be stored as cookies, but the cookie is only the storage mechanism, and not serving any role in the authentication of the user.
>
> JWT (Json Web Tokens) format:
>
> header.payload.signature
>
> MORE INFO: http://stackoverflow.com/questions/17000835/token-authentication-vs-cookies

What is local storage?
> Persistent data stored on a client's machine. Local storage has no expiration (Session storage is cleared when a broweser is closed), nor does it have a small size restriction, like cookies. No local storage information is automatically sent to the server.

What is CORS?
> Cross Origin Resource Sharing
>
> A standard that allows restricted resources to be requested from domains outside of the domain where the resource was first served. For security reasons, browsers restrict cross-origin HTTP requests initiated from within scripts ("Same Origin Policy"). CORS allows servers to describe the set of origins that are permitted to read information using a web browser.  
>
> More Info: https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS

What is XSS? Give an example
> Cross Site Scripting
>
> An attack that allows users to inject client side javascript into webpages viewed by other users. A classic example is a site search engine: if one searches for a string, the search string will typically be redisplayed verbatim on the result page to indicate what was searched for. If this response does not properly escape or reject HTML control characters, a cross-site scripting flaw will ensue.
>
>  XSS attacks can be reflected (non-persistent) or persistent. Reflected attacks cause the victims browser to execute the included scripts, and affect their local machine. A reflected attack is typically delivered via email or a neutral web site. The bait is an innocent-looking URL, pointing to a trusted site but containing the XSS vector. If the trusted site is vulnerable to the vector, clicking the link can cause the victim's browser to execute the injected script. Persistent attacks occur when the data provided by the attacker is saved by the server, and then permanently displayed on "normal" pages returned to other users in the course of regular browsing, without proper HTML escaping. A classic example of this is with online message boards where users are allowed to post HTML formatted messages for other users to read.
>
> More Info: https://en.wikipedia.org/wiki/Cross-site_scripting
>
> More Info: https://www.youtube.com/watch?annotation_id=annotation_3275345267&feature=iv&src_vid=vRBihr41JTo&v=L5l9lSnNMxg

What are CSRF attacks? Give an example
> Cross Site Request Forgery
>
> A type of attack that occurs when a malicious web site, email, blog, instant message, or program causes a user’s web browser to perform an unwanted action on a trusted site for which the user is currently authenticated. CSRF attacks are used by an attacker to make a target system perform a function via the target's browser without knowledge of the target user. CSRF attacks specifically target state-changing requests, not theft of data, since the attacker has no way to see the response to the forged request.
>
> For example, an attacker could use a hidden form to send a specific POST request, with the data filled in by the attacker, and disguise the form submission as an innocuous link. The victim would have to be authenticated in a other tab or window to the site where the form is being submitted.
>
>To protect against CSRF attacks, servers can check Referrer headers, or implement "nonce" tokens: single use, randomly generated strings that authenticate form submissions.

> More Info: https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)_Prevention_Cheat_Sheet
>_
> More Info: https://www.youtube.com/watch?v=vRBihr41JTo

What is cross browser compatibility?
> When a web site or app looks and behaves the same way no matter what platform is used to view it. This means supporting browsers from different companies, older versions of these browsers, and browsers on different types of hardware (Mac, PC, mobile, etc.)


In as much detail as possible, explain what happens when I type 'google.com' into my navbar and hit enter.
  > - Browser constructs an HTTP request
    - Browser makes a DNS lookup to find the IP
    - There's a TCP handshake with the server
    - The HTTP request is sent from my browser to the server
    - A Google server receives the request, probably in a load balancer of some sort
    - Forwards it on until it eventually gets to a server that processes the homepage
    - Server generates an HTTP response and sends it back to the browser
    - Browser parses the HTTP response, turns HTML into DOM, then visually draws the page
    - For every image, script tag etc., it checks the browser cache and makes new HTTP requests for everything missing

What are the 3 data sources that the params hash is compiled from?
>path variables, request body, and query string.

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
