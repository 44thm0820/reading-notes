# Reading: Component Based UI readingnotes due apr25

Below you will find some reading material, code samples, and some additional resources that support today's topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

## Review, Research, and Discussion

In your reading notes page for this class, provide answers to the following prompts. Cite any external sources

1. Name 5 Javascript UI Frameworks (other than React)
1. What's the difference between a framework and a library?

### Document the following Vocabulary Terms

| Term                            |
| ------------------------------- |
| Rendering                       |
| Templates                       |
| State                           |

## Preview

Skim the following materials in preparation for the upcoming lecture. Note the following as you browse the material, and be prepared to participate in discussions during lecture

1. Which 3 things had you heard about previously and now have better clarity on?
1. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
1. What are you most excited about trying to implement or see how it works?

### Preparation Materials

- [react hello world](https://facebook.github.io/react/docs/hello-world.html){:target="_blank"}

This webpage is a rehash of what we learned in 301 JavaScript.  It serves to reintroduce what we already learned: The smallest React example:

``` js
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<h1>Hello, world!</h1>);
```

- [introducing JSX](https://facebook.github.io/react/docs/introducing-jsx.html){:target="_blank"}

This webpage is a rehash of what we learned in 301 JavaScript.  It serves to reintroduce what we already learned: The variable declaration:

```js
const element = <h1>Hello, world!</h1>;
```

JSX is a syntax extension to JS. JSX produces React "elements."
React does not require JSX, but most people find JSX helpful as a visual aid when working with UI inside JS code.  It allows React to show more useful and warning messages.
Other reminders what JSX is:
JSX preevents injection attacks.
JSX represents objects.


- [rendering elements](https://facebook.github.io/react/docs/rendering-elements.html){:target="_blank"}

Elements are the smallest building blocks of React apps.

An element describes what you want to see on the screen:

```js
const element = <h1>Hello, world</h1>;
```

Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

#### Bookmark

- [sass cheatsheet](https://devhints.io/sass){:target="_blank"}
- [react cheatsheet](https://devhints.io/react){:target="_blank"}
- [another react cheatsheet](https://reactcheatsheet.com/){:target="_blank"}