# Readings: Express - class02 - 401

## Note from the student Rey Mercado to the grader
Supplemental guidance not provided in canvas for class02 reading assignment was found in the class repo at

 https://github.com/codefellows/seattle-javascript-401d46/blob/main/class-02/DISCUSSION.md . 
 
 I have effectively merged the two documents in order to best provide a quality submission for class 02 readings.

## Overview

Below you will find some reading material, code samples, and some additional resources that support today’s topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

## Review, Research, and Discussion

In your reading notes page for this class, provide answers to the following prompts. Cite any external sources

1. What's the difference between `PUT` and `PATCH`?
1. Provide links to 3 services or tools that allow you to "mock" an API for development like `json-server`
1. Compare and contrast Swagger and APIDoc.js
1  Which HTTP status codes should be sent with each type of (un)successful API call?
1. Compare and contrast SOAP and ReST

### Document the following Vocabulary Terms

| Term                            |
| ------------------------------- |
| Web Server                      |
| Express                         |
| Routing                         |
| WRRC                            |

## Preview

Skim the following materials in preparation for the upcoming lecture. Note the following as you browse the material, and be prepared to participate in discussions during lecture

1. Which 3 things had you heard about previously and now have better clarity on?
1. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
1. What are you most excited about trying to implement or see how it works?

## Reading

### ****[An introduction to NodeJS and Express - mdn](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)****

This article is from MDN intends to provide an introduction what NodeJS and Express is all about.  As MDN already has a authoritative reputation of providing accurate and clear documentation among JavaScript developers for several years now, my first impression by looking at the page and layout is that the article will not disappoint me when I read this article in making I am informed of what I need to know regarding the topic NodeJS and Express.

The article has on its left side of its webpage a navigation / bookmark section bar of some sort that informs me of the various topics that will be covered before the article concludes. They are:

1. Introducing Node
2. Web Frameworks
3. Introducing Express
4. Where did Node and Express come from?
5. Is Express opinionated?
6. What does Express code look like?
7. Summary

Node is:
 - open-source
 - cross-platform
 - runtime environment
 - allows creation of many kinds of server-side tools and applications in JavaScript

Node's runtime is intended for use outside of a browser context, for example, running directly on a computer or a server operating system.

Node does not include browser-specific JavaScript APIs.

Instead, Node adds support for more traditional OS APIs such as HTTP and file system libraries.

Node's selling points from a web server development perspective include
- great performance, designed to optimize throughput and scalability in web applications
- written in JavaScript, the same language as the browser's language is written, which avoids "context shift" when adopting something different than Node that requires learning another programming language.
- by using JavaScript, Node takes advantage of the JavaScript language ecosystem which evolves more rapidly and adopts more easily the latest improvements in programming design compared to other web-server languages such as Python or PHP. Many popular languages compile or convert into JavaScript by design, including TypeScript, CoffeeScript, ClojureScript, Scala, LiveScript, etc.
- the node package manager provides access to hundreds of thousands of reusable packages.
- node.js is portable and is readily available on many popular operating systems such as Windows, macOS and Linux, and also supported well by many web hosting providers.

Node.js can be used to create a simple web server using the Node HTTP package.

However, other common web-development tasks are not directly supported by Node. Specific handling for different HTTP verbs (get, post, delete, etc.), or handling requests at different URL paths ("routes"), serving static files, using templates to dynamically create the response, are not supported by Node and instead web frameworks or writing the code onesself are the only solutions.

Express is one of such frameworks and that is a Node web framework most popular of all Node web frameworks. Many other popular Node web frameworks use Express's library.

Express provides capabilities to:
- Write handlers for requests with different HTTP verbs at different URL paths (routes).
- Integrate with "view" rendering engines in order to generate responses by inserting data into templates.
- Set common web application settings like the port to use for connecting, and the location of templates that are used for rendering the response.
- Add additional request processing "`middleware`" at any point within the request handling pipeline.

Node and Express first appeared in 2009-2010 timeframe, with Node in 2009 and and Express in 2010.

Express docs boast on its website several high profile companies that use Express in production including: accenture, IBM, MuleSoft, Uber, and Fox Sports. See webpage https://expressjs.com/en/resources/companies-using-express.html 

Express is unopinionated, when it comes to categorizing a web framework between opinionated and unopinionated. Because Express is unopinionated, Express has fewer restrictions on how to form components together, makes it easier for developers to optimize the most suitable tools to complete a task. For example express allows you to insert almost any compatible middleware into the request handling chain in almost any order of preference.

Express code looks like this:

more to follow - placeholder

### ****[What is NPM? - npmjs docs](https://docs.npmjs.com/getting-started/what-is-npm)****

placeholder

### ****[What is TDD? - agile glossary](https://www.agilealliance.org/glossary/tdd/)****

placeholder

### ****[CI/CD - video](https://www.youtube.com/watch?v=xSv_m3KhUO8)****

placeholder

<br>

## Bookmark and Review

### [nodeJS docs](https://nodejs.org/en/docs/)

### [npm docs](https://docs.npmjs.com/)

### [express docs](https://expressjs.com/en/4x/api.html)

### [http status codes](https://www.restapitutorial.com/httpstatuscodes.html)

### [supertest](https://github.com/visionmedia/supertest)