# General Programming Questions

## Resources

- [What I Learned Doing 250 Interviews at Google](https://www.youtube.com/watch?v=r8RxkpUvxK0)
- [How to Prove Your Skills During an Interview](https://www.youtube.com/watch?v=i6mb4pZxNGM)

What is JSON?
>_

What is REST?
>_

What is HTTP?
>_

What is TCP?
>_

What is an API?
> Application programming interface. The publicly exposed and programmable part of an application.

Explain how the web works
>_

Explain REST
>_

Explain statelesness
>_

Explain the anatomy of a HTTP request & response
>_

Explain browser caching
>_

What are cookies? What role do they play in web apps?
>_

What is local storage?
>_

What is CORS?
>_

What are CSRF attacks? Give an example
>_

What are web tokens?
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

What is 595 in binary?
>1001010011

Convert 101101 to base 10
>45

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
