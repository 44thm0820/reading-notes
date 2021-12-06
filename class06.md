# Readings: Node.JS - Class06

## Reading

https://www.sitepoint.com/an-introduction-to-node-js

1. What is node.js?
It's a JavaScript runtime. It's a program we use to execute JavaScript on our computers.

2. In your own words, what is Chrome’s V8 JavaScript Engine?
Chrome's V8 JavaScript Engine is a performance-centric program that runs in Google Chrome and other Chromium-based web browsers, that compiles JavaScript so that our computers can use JS.

3. What does it mean that node is a JavaScript runtime?
node allows the execution of JavaScript on our computer rather than just the browser.

4. What is npm?
npm is the JavaScript Package Manager as well as the world's largest software registry.

5. What version of node are you running on your machine?
typing node -v, I got v14.17.5

6. What version of npm are you running on your machine?
typing npm -v, I got 7.24.1

7. What command would you type to install a library/package called ‘jshint’?
npm install -g jshint

8. What is node used for?

 One use of Node is installing via npm and running via Node various build tools designed to automate the process of developing a modern JavaScript application.  Webpack, ESLint, Gulp.js, Mocha, and Chai are common build tools found by using node.

 Node also allows server-side programs to be written in JavaScript. It can be used as a scripting language.  It is suited to building applications that require real-time interaction or collaboraration like chat sites.

 Node is single-threaded but also event-driven. If node encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event.  When the I/O operation has finished (another kind of event), the server will execute the callback and continue working on the original request.

 Thusly, Node has asynchronous (non-blocking behavior).

 Node's execution model causes the server very little overhead, compared to traditional servers such as Apache, PHP, or Ruby, which block execution of subsequent I/O operations until the current operation completes.


https://www.codefellows.org/blog/6-reasons-for-pair-programming/
1. What are the 6 reasons for pair programming?

- Greater Efficiency - research shows higher-quality code for a slightly longer duration
- Engaged collaboration - augments engagement for both programmers
- Learning from fellow students - forces teaching or learning for communication for both
- Social skills - improves interpersonal skills, qualities employers look for
- Job interview readiness -skills improved in pair programming are what employers interviewi for
- Work environment readiness - skills on day-to-day work pairing puts someone more qualified than a cs grad with no prior experience pairing

2. In your experience, which of these reasons have you found most beneficial?
I don't have much experience in the industry, but have pair programmed before... I'd say though work environment readiness... it saves costs for employers when not much investment needed to train someone who has experience collaborating in programming.

3. How does pair programming work?
One is designated the driver, and the other is designated the navigator.  The driver is the programmer who types, including controlling the text editor, switching files, version control and what gets written.
The navigator vocalizes guidance to the driver but does not provide direct input to the computer.  The navigator is expected to focus on the big picture, anticpating what comes next, how algorithm may be converted to code, while reviewing driver's code for typos or bugs. The navigator uses the time not typing to also research documentation, and solutions on a browser.


# Bookmark/Skim
-https://locationiq.com/
I looked at the docs https://locationiq.com/docs
provides an API to geolocate for a better UI experience

-https://www.npmjs.com/package/axios
Axios is a promise based HTTP client for the browser and node.js
sample code is
```
import axios from "axios";
axios.get('/users')
  .then(res => {
    console.log(res.data);
  });
```

https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await


## Code Samples
```
import axios from "axios";
axios.get('/users')
  .then(res => {
    console.log(res.data);
  });
```

## Additional Resources
https://markdownguide.org/cheat-sheet


## Things I want to know more about
I want review async/await and axios after reading the docs from hyperlinks above