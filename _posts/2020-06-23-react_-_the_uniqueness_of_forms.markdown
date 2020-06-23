---
layout: post
title:      "React - The Uniqueness of Forms"
date:       2020-06-23 18:05:19 +0000
permalink:  react_-_the_uniqueness_of_forms
---


If you're far enough in web application development to understand React, you've probably noticed that forms are handled a bit different from other technologies such as Ruby on Rails. Where forms would normally handle data entirely  based on what is being sent as an HTTP request, React offers a different approach via components which *handle all input values based on state.* I won't go into the overly-technical side of how this works, so let's just settle on this truth -- state, in this case, is used as a way for us to control form values. React also includes built-in event listener tools that help to set our state every single time our form changes. For forms, the best practice is to use `onChange`. According to the [documentation](https://reactjs.org/docs/dom-elements.html#onchange), 

> The `onChange` event behaves as you would expect it to: whenever a form field is changed, this event is fired. We intentionally do not use the existing browser behavior because `onChange` is a misnomer for its behavior and React relies on this event to handle user input in real time.
> 

Let's take a look at how this might look in JSX inside of your component:

```
<input type="text" onChange={event => this.handleFirstNameChange(event)} value={this.state.firstName} />
<input type="text" onChange={event => this.handleLastNameChange(event)} value={this.state.lastName} />
```

In this example, we are handling two events: Any change to our form's `firstName` and `lastName`. In order for us to handle this state change, we can direct our event handles to Anonymous Functions, or "Arrow Functions". See below:

```
handleFirstNameChange = event => {
  this.setState({
    firstName: event.target.value
  })
}
 
handleLastNameChange = event => {
  this.setState({
    lastName: event.target.value
  })
}
```

This is exciting! Now we can see our state is handling all updates when something changes in our form. The initial state is set at the top of our class, which looks like this:

```
class Form extends React.Component {
  state = {
    firstName: "John",
    lastName: "Henry"
  }
```

There is something particularly important in the code snippet above that needs to be taken into consideration. Our `firstName` and `lastName` both have a pre-defined value. Our form will function on the front end exactly as a user would expect it to, but our `state` will increment those value updates on the information presented in the back end. If a user were to type "Sarah" as her first name, our `state`'s value of `firstName` would save as `JohnSarah`. A good rule of thumb to go by is to leave your `state` values predefined as an empty string to avoid this issue.

Now that we've covered the updating aspect of our form `state`, surely there must be a way to handle submitting the form! The good news is -- there is! We guide our attention towards the next event handler in React called `onSubmit`. Here's a visual on what that might look like in our component:

```
render() {
  return (
    <form onSubmit={event => this.handleSubmit(event)}>
      <input
        type="text"
        onChange={event => this.handleFirstNameChange(event)}
        value={this.state.firstName}
      />
      <input
        type="text"
        onChange={event => this.handleLastNameChange(event)}
        value={this.state.lastName}
      />
    </form>
  )
}
```

Now we've got a new anonymous function defined to help handle this event called `this.handleSubmit(event)`.

```
handleSubmit = event => {
  event.preventDefault()
  let formData = { firstName: this.state.firstName, lastName: this.state.lastName }
  this.sendFormDataSomewhere(formData)
}
```

You'll find the first task in this function is calling on our `.preventDefault()` method found in vanilla JavaScript. The default process of a form is to submit its data & refresh the page. Since there is no need for this to happen in React, we stop that action. Additionally, we have another anonymous function defined as `this.sendFormDataSomewhere(formData)`. Which, this is where we will handle our fetch requests. Fetch requests in React are something we can cover in a future blog post, but just know this is where we will be able to handle data between the front end and back end API of our application.

Forms in React offer much more flexibility than what is covered in this blog post! Check out the full [documentation](http://https://reactjs.org/docs/getting-started.html). If you're a developer who takes your work seriously and strive for efficiency, you're definitely looking in all the right places with React!


