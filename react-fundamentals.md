### Remember

Answer these on your own, then compare answers as a group

1.  What is React?
  -React is a Javascript library that allows developers to quickly and efficiently build stateful applications that tightly control the flow of data.

2.  What is create-react-app?
  -create-react-app is a command line tool that automatically installs all the libraries and dependencies needed to run a React app.
  
3.  What is Component Based Architecture?
  -Component Based Architecture is a UI paradigm that is based around the concept of reusability of code and abstraction of UI elements.
  
4.  What is JSX?
  -JSX stands for JavaScript XML.  It allows developers to write HTML and XML inside React apps, but compiles down to Javascript for run-time.

5.  What is the virtual DOM?
  -The virtual DOM is a copy of the DOM that React runs in memory.  Modifications to the virtual DOM are kept track of by React, and applied to the DOM as neccessary, allowing the app to run faster.

6.  What is unidirectional (one-way) data flow?
  -Unidirectional data flow is a way of controlling data in React that limits data to only components that need it, and that component's children, if they need it.  That way, data flows down, from parent to child, but never up from child to parent.

### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`
  -'create-react-app my-app' creates a folder in the current directory named 'my-app', then downloads and installs in that directory all of the libraries and dependencies neccessary for running a bare bones React app.  It also creates a git repository in that same folder.

8.  Explain what this code does:

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```
  -Creates a stateless functional componenet called Mentor that takes in one prop from the parent called 'title'

9.  Explain how data is passed from a parent component to a child component.

### Apply

Try these on your own, but work together if you start to get stuck.

10.  Use `create-react-app` to create a new React application called `student-directory`

11.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

12. What are the benefits and drawbacks of using a tool like create-react-app?

13. Compare and contrast JSX with other templating options, such as those used in Angular or Vue

14. Compare and contrast one-way data flow with two-way data binding.
