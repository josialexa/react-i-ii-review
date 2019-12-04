### Remember

Answer these on your own, then compare answers as a group

1.  What is state?
  -State is data that is local to the current component.  It can be passed down to children as props, and cannot be modified directly.

2.  Where do you set initial state?
  -Initial state is set in the constructor of the component its needed for, specifically in the state object.

3.  What method do you use to update state?
  -this.setState().

### Understand

Discuss this question in pairs if you have a 4-person group

4.  Explain what's happening in this component.

```jsx
import React, { Component } from "react";

class LeadMentor extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questionsAnswered: 0
    };

    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    this.setState({ questionsAnswered: this.state.questionsAnswered + 1 });
  }
  render() {
    <div className="lead-mentor-container">
      <h1>Tim Biles</h1>
      <h3>{this.state.questionsAnswered}</h3>
      <h3>questions answered today</h3>
      <button onClick={this.handleClick}>Increase Answers</button>
    </div>;
  }
}
```

  -This creates a component that displays the number of times the 'Increase Answers' button has been clicked, and increases that number by one for each click.

### Apply

Try these on your own, but work together if you start to get stuck.

5.  Create a `Student` component that keeps track of the number of questions the student has asked, with a button that adds 1 to the total when it's clicked

```jsx
import React, {Component} from 'react'

export default class Student extends Component {
  constructor() {
    super()
    this.state = {
      questionsAsked: 0
    }
    this.handleClick = this.handleClick.bind(this)
  }
  handleClick() {
    this.setState({
      questionsAsked: this.state.questionsAsked + 1
    })
  }
  render() {
    return (
      <div>
        <div>
          <span>{this.state.questionsAsked}</span>
        </div>
        <div>
          <button onClick={this.handleClick}>Ask Question</button>
        </div>
      </div>
    )
  }
}
```

6.  Now add a text input where the student can type in their questions with a button to add them to a list of questions that is displayed below the number of questions asked.

### Analyze, Evaluate, Create

Discuss these questions as a group

7.  Could your `Student` component be refactored into a functional component? Why or why not?

8.  What are the pros and cons of using a class method for an event handler vs. using an arrow function inline?

9.  The render() method is called every time a component's state is updated. For a text input, that means the render method is called for every keypress. Why isn't this bad for performance?
