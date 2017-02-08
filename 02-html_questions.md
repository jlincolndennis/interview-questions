# FHTML Questions

## Resources / sources

- http://www.toptal.com/html5/interview-questions
- http://www.skilledup.com/articles/html-html5-interview-questions-answers
- http://www.codeproject.com/Articles/702051/important-HTML-Interview-questions-with-answe
- http://www.sitepoint.com/10-typical-html-interview-exercises/
- http://career.guru99.com/top-50-html-interview-questions/
- http://www.geekinterview.com/Interview-Questions/Web/Html
- http://techpreparation.com/html-interview-questions-answers1.htm#.VlmapN8rLXE
- http://www.careerride.com/Interview-Questions-HTML.aspx


What is HTML?
> Hyper Text Markup Language
>
> A standardized system for annotating text files to create webpages and web applications. Browsers parse HTML and use it to create the DOM and render the webpage for the user. HTML provides structure and formatting for the content of a webpage.

What is the difference between HTML elements and tags?
> An HTML document contains tags, such as `<p></p>` which are used to render elements. Generally, elements begin at a opening tag (ie `<p>`), and end at a corresponding closing tag (`</p>`).

What is “Semantic HTML?”
> The use of specific HTML tags and patterns to communicate then context and meaning of a web document, in addition to its format and styling. Semantic HTML is particularly useful in providing context for accessibility software that assists handicapped or disables users.

What does DOCTYPE mean?
> The DOCTYPE declaration tells the browser (or other browsing agent) what kind of document the web file is. This ensures that the browser correctly parses the HTML and renders the page as intended by the developer.

What is the DOM?
> Document Object Model. Tree representation of all HTML elements on a webpage that creates the structure of a webpage, and what HTML gets parsed into.

Describe event bubbling.
> After an event is triggered on a specific element, it travels up the DOM and alerts parent elements in nesting order.
>
> Event delegation allows you to avoid adding event listeners to specific nodes;  instead, the event listener is added to one parent.

Explain and contrast the usage of `event.preventDefault()` and `event.stopPropagation()`. Provide an example.
> `preventDefault()` stops an event from executing its default behavior when triggered, for example, a link from triggering a state change. `stopPropagation()` stops an event from "bubbling" up the DOM, where it might trigger other events or default behaviors.

What are data-attributes and why are they useful?
> Data attributes are part of HTML5 that let you place information on a DOM object so that you can easily recall it later in your code, or with some other DOM interaction.

> For example if you want to store an ID for a specific `div` but don't want it to appear visible on the page. Before HTML5, you had to store data in class or rel attributes, which sometimes caused problems.

What is minification?
> The act of removing all unnecessary characters in a code file (whitespace, comments, etc.), while not changing its functionality. JavaScript is typically minified when served to decrease the amount of data that needs to be sent and received over network connections.


What's the difference between one-way and two-way binding?
> Two-way binding is when a UI input is bound to a model, and they are allowed to update each other directly. One-way binding, the model tells the input what to display (single source of truth) and is updated via events.

Explain the same-origin policy with regards to JavaScript.
> For security reasons, browsers restrict cross-origin HTTP requests initiated from within scripts. CORS allows servers to describe the set of origins that are permitted to read information using a web browser.  Scripts from different origins can execute malicious code that attempt to access or modify DOM elements on the target origin page.

What is a Single Page Application?
> A single page app is a web application that requires only one call the server to download enough data to render all the different views needed for the app. When a user initiates a state change, rather than submitting a new HTTP request, the new state is programmatically rendered on the client side.

What's the difference between standards mode and quirks mode?
> Standards mode renders webpages based on the current W3C standards. Quirks mode emulates non-standard behavior in order to render webpages created by W3C standards existed. Browsers by different vendors might implement Quirks most differently. Browsers use the DOCTYPE declaration (or the lack thereof) to determine which mode to use.

What's the difference between HTML and XHTML?
> XHTML is basically HTML that follows all the rules of XML (as XHTML is in the same family as XML). XML is generally a stricter mark up language, and XHTML was an attempt to bring that strictness to HTML. Prior to HTML5, HTML was defined as an application of Standard Generalized Markup Language (SGML), while XHTML was an application of XML. Major differences include that in XML all tags must be explicitly closed, "attribute shortening" is not allowed and in XML, all markup must be lowercase.

What are the limitations when serving XHTML pages?
> IE versions 8 and earlier do not fully support XHTML.

Describe the difference between a cookie, sessionStorage and localStorage.
> Cookies are small, size restricted pieces of data sent from a web server and stored in a user's browser. Cookies allow browsers to remember stateful information. A cookies expiration varies based on the type and the expiration duration can be set from either server-side or client-side (normally from server-side).
>
> `sessionStorage` data is removed when a browser session ends, usually signified by closing the browser window.
>
> `localStorage` does not have a small size restriction and is never automatically removed.
>
> Cookies are primarily for server-side reading (can also be read on client-side), localStorage and sessionStorage can only be read on client-side.

Describe the difference between `<script>`, `<script async>` and `<script defer>`.
> Normal execution `<script>`: This is the default behavior of the `<script>` element. Parsing of the HTML code pauses while the script is executing. For slow servers and heavy scripts this means that displaying the webpage will be delayed.
>
> Deferred execution `<script defer>`: Delays script execution until the HTML parser has finished. A positive effect of this attribute is that the DOM will be available for your script.
>
> Asynchronous execution `<script async>`: HTML parsing may continue and the script will be executed as soon as it’s ready.
>
> [More Info](http://stackoverflow.com/questions/436411/where-should-i-put-script-tags-in-html-markup/24070373#24070373)

Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`?
> The `<link>` tag does not define the actual structure of a web document, and therefore should only be put in the `<head>`. Putting the `<link>` tag in `<head>` is part of the W3C standard.
>
> Placement of `<script>` tags is actually is a more nuanced and debated topic. When placing actual code between script tags, especially is that code manipulated the DOM, is is generally best to place them just before the closing `<body>` tags, because HTML is rendered from the top down, and scripts that occur at the top of the document will be run before the DOM objects they attempt to manipulate have been rendered.
>
> `<script>` that load external JS files and libraries may be placed in the head, and their placement and method of execution can be fine tuned using `<script async>` and `<script defer>`. See above answer and check [here](http://stackoverflow.com/questions/436411/where-should-i-put-script-tags-in-html-markup/24070373#24070373) for more information.

What is progressive rendering?
> Progressive rendering is the name given to techniques used to render content for display as quickly as possible.
>
> Examples of such techniques :
> 
>Lazy loading of images where (typically) some javascript will load an image when it comes into the browsers viewport instead of loading all images at page load.
>
>Prioritizing visible content (or above the fold rendering) where you include only the minimum css/content/scripts necessary for the amount of page that would be rendered in the users browser first to display as quickly as possible, you can then use deferred javascript (domready/load) to load in other resources and content.

What are some of the key new features in HTML5?
>_

What are “web workers”?
>_

How do you indicate the character set being used by an HTML5 document? How does this differ from older HTML standards?
>_

Discuss the differences between an HTML specification and a browser’s implementation thereof.
>_

Briefly describe the correct usage of the following HTML5 semantic elements: `<header>`, `<article>`, `<section>`, `<footer>`.
>_

Can a `<section>` contain `<article>` elements? Can an `<article>` contain `<section>` elements? Provide usage examples.
>_

Can a web page contain multiple `<header>` elements? What about `<footer>` elements?
>_

Describe the relationship between the `<header>` and `<h1>` tags in HTML5.
>_

Give a simple implementation of the `<video>` tag to embed a video stored at `http://www.example.com/amazing_video.mp4`. Give the video a width of 640 pixels by 360 pixels. Provide the user with controls.
>_

Write the code necessary to create a 300 pixel by 300 pixel `<canvas>`. Within it, paint a blue 100 pixel by 100 pixel square with the top-left corner of the square located 50 pixels from both the top and left edges of the canvas.
>_

How do you make comments without text being picked up by the browser?
> `<!-- Place your comment between these thingies -->`

What is the difference between linking to an image, a website, and an email address?
>_

What is the syntax difference between a bulleted list and numbered list?
> For bulleted list, wrap the `li` elements in a 'ul' tag. For a numbered list, wrap `li` elements in a `ol` tag.

What is the difference between `<div>` and `<frame>`?
>_

What is the difference between the application model of HTML and HTML5?
>_

Ok, what’s the real difference between HTML and HTML5?
>_

What are some new HTML5 markup elements?
>_

What elements have disappeared?
>_

What are the new media-related elements in HTML5?
>_

What are the new image elements in HTML5?
>_

What is the difference between SVG and `<Canvas>`?
>_

What are some of the major new API’s that come standard with HTML5?
>_

What is the difference in caching between HTML5 and the old HTML?
>_

What are some templating libraries.
>

What's the difference between feature detection, feature inference, and using the UA string?
>

How do you handle internationalization?
>
