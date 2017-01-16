# Back End Questions

## Resources / sources

- https://blog.risingstack.com/node-js-interview-questions/
- http://www.toptal.com/nodejs/interview-questions
- http://www.tutorialspoint.com/mongodb/mongodb_interview_questions.htm


### Git

What's version control?
>_

Teach me how to use version control.
>_

### Node

What is an error-first callback?
>_

How can you listen on port 80 with Node?
>_

What's the difference between operational and programmer errors?
>_

Why npm shrinkwrap is useful?
>_

How does Node.js handle child threads?
>_

What is the preferred method of resolving unhandled exceptions in Node.js?
>_

How does Node.js support multi-processor platforms, and does it fully utilize all processor resources?
>_

What is typically the first argument passed to a Node.js callback handler?
>_

What is npm?
>_

What `package.json`?
>_

What is nodemon? Why is it so helpful?
>_

Explain module.export
>_

### Express

Name two objects that are NOT available to us in Node.js (that are available in the browser).
>

What is Express JS?
>

Why do we add the text `"node_modules"` to our `.gitignore`?
>

What does the --save flag do when we install modules with npm?
>

What is localhost?
>

What is HTTP?
>

Explain GET request vs POST request
>

Explain render vs redirect
>

What is a route?
>

What is EJS?
>

Where do static assets (images, javascripts, stylesheets) go?
>

What is the difference between `require("express")` and `require("./express")`?
>

What is middleware?
>

What does `body-parser` enable us to do?
>

What is the difference between `req.params`, `req.query` and `req.body`?
>

Why can't we use jQuery in our server code (app.js)?
>

Explain method_override
>

Explain cookies vs sessions
>


What are the variables available to a program (usually server-side) that aren't actually written in the program itself?
> Environment Variables

What is an ORM?
>Object Relationship Mapping, it connects data in your database with functionality in your models to create objects.

>An ORM (for object relational mapping) is a tool that lets you access and change data from a database using an object paradigm. Instead of writing raw SQL and talking to the database directly yourself, you use an ORM to produce the code needed to interact with the database. ActiveRecord serves this purpose for Rails.

What is a relational database and how does it differ from a non-relational database?  Give examples
>Relational databases are composed of various tables that are 'related' by associations made from among the table entries. Non-relational databases have no table schema, instead they have individual models within whichall associated data is contained. Any SQL database is relational, MongoDB is an example of a non-relational DB.

>A relational database is based on the relational model. It organizes data into tables of columns and rows. Each one of these rows will have its own key. It's because of these keys that we can link a row to another by using its key, or as its called "a foreign key". Relational databases use SQL to query and change the database

>Examples: PostgreSQL, MySQL.

>A non-relational db does not use the same table/key model as a relational one. These types of databases are made to scale and handle much large amounts of data. Rather than use tables/keys, they use their own special frameworks.
