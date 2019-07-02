# React Assessments

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. Here is a list of pros and cons to using the React library to build your application -- but some of them are false. Remove the false statements from the list:

- React was created to be simple, so that even people with minimal code experience could use it and create Single Page Applications (SPAs)
- React is a modern, efficient answer to complex UI applications

- React is a flexible library that plays the role of V in an MVC framework

 
 #### 2. What are "smart"(logic) and "dumb"(display) components? Explain the difference and also add why we bother to make the distinction between them.
 
 
 //Your Answer
 A smart component is a component with state in it, and it manages updates and responses.
 A dumb component has no states and typically is only used to display.
 
 //Googled Answer (from https://medium.com/@thejasonfile/dumb-components-and-smart-components-e7b33a698d43)
 
"Smart Components
Smart components (or container components) on the other hand have a different responsibility. Because they have the burden of being smart, they are the ones that keep track of state and care about how the app works.
Using the container design pattern, the container components are separated from the presentational components and each handles their own side of things. The container components do the heavy lifting and pass the data down to the presentational components as props.
They are class-based components and have their own state defined in their constructor() functions."

"Dumb Components
Dumb components are also called ‘presentational’ components because their only responsibility is to present something to the DOM. Once that is done, the component is done with it. No keeping tabs on it, no checking in once in a while to see how things are going. Nope. Put the info on the page and move on.
The components themselves only have a render() method (they don’t need any others) and are often just Javascript functions. They don’t have internal state to manage. They wouldn’t know how to change the data they are presenting if they were asked. Ignorance is bliss."
 
#### 3. When we use "yarn add ..." in the terminal - what is yarn doing? And what file will always be automatically updated after we add a package with yarn?
 
 
 //Your Answer
 I do not remember what "yarn add ..." does
 
 //Googled Answer (from https://yarnpkg.com/en/docs/cli/add)
 
 "In general, a package is simply a folder with code and a package.json file that describes the contents. When you want to use another package, you first need to add it to your dependencies. This means running yarn add [package-name] to install it into your project.

This will also update your package.json and your yarn.lock so that other developers working on the project will get the same dependencies as you when they run yarn or yarn install.

Most packages will be installed from the npm registry and referred to by simply their package name. For example, yarn add react will install the react package from the npm registry."
 
 
#### 5. There are three mistakes in this code that would cause it to break our application. Find the mistakes and fix them:

 import React, { Component } from 'react';

class Recipes extends Component {
  constructor(props){
    super(props)
    this.state = {
      recipes: 
      [{name: 'Meatballs'}, {name: 'Mac & Cheese'}]
    }
  }

  render() {

    return (

      let recipes = this.state.recipes.map(function(recipe,index){
        return(
          <li key={index}>{recipe.name}</li>
        )
      })

      <ul>
        recipes
      </ul>
    );
  }
}

export default Recipes;

#### 6. Name three html input types. (NOTE: text is the default type - so it doesn't count in this case)
 
 //Your Answer
 Button
 Image
 ???
 
 //Googled Answer
 
 Checkbox
 Color
 Date
 Email
 Month
 Number
 Password
 Week
 Time
 URL
 Search
 Submit
 
 #### 7. How would you explain state to a friend who doesn't know code?
 
 //Your Answer
 A state of a component is a snapshot of the attributes of that component at a certain point in time. 
 For example, one state of a component called "Car" could be lights: off. So, at this current point in time, the cars lights are off.
 States can be set and updated. For example, a car could have a function that changes its state of "lights" from "off" to "on".
 
 //Googled Answer (from https://medium.com/the-andela-way/understanding-the-fundamentals-of-state-in-react-79c711be677f)
 
 What is State?
State is a JavaScript object that stores a component’s dynamic data and determines the component’s behaviour. Because state is dynamic, it enables a component to keep track of changing information in between renders and for it to be dynamic and interactive.
State can only be used within a class component. If you anticipate that a component will need to manage state, it should be created as a class component and not a functional one.
 
 #### 8. What is the difference between component state and props? Your answer should include a short explanation of both.
 
 //Your Answer
 Component state is an instance of a component which describes certain attributes. 
 State can be set within a method or otherwise to an updated value - thus, it can constantly be updated again and again.
 
 A components' props describe information that it has received from a parent component, and it can use this information.
 If a child component receives its props from a parent component's state, as that state is updated, so is the child components' prop.

 //Googled Answer (from https://medium.com/@decode2018/props-vs-state-react-64fcf6c55886)
WHAT ARE PROPS? WHAT IS STATE?
Props, short for “properties” are single values, or objects containing values that can be defined or “stated” in a Parent component and passed down to its Children almost similar to how real parents pass down physical traits to their children. They are immutable (non-changing) but trigger state changes…that can then in turn change the prop itself (more on this later)!
State on the other hand is defined and changed in the component that contains the state so we can look at state as being “private”. We can change and should only change state by using the function setState().
   
#### 9. Write a paragraph or so about your experience with building tic-tac-toe. Some topics to start with might be: things you learned about yourself, concepts from React that stood out to you, something about pair programming (if you paired), or the experience of building something in code from scratch.

I had a good experience building the treasure hunt with my group. It was an interesting experience because we were, at times, breezing through the features, but there were a few bugs and errors that we spent a long time trying to fix. For example, we tried to put in a reset button, but because of the way that we had built our components and used state, it was not easy. We ended up moving all of our logic down from parent to child, and troubleshooted for a total of around 5 hours. However, I am proud of my group for not giving up and for trying to solve the problem for such a long time - my group members showed a lot of perseverance and patience. The learning experience I had during the group was to try and understand what Josh was trying to do. He often had an idea of what to do, and would try to explain it verbally, and I wouldn't understand, but after watching him do it, I was able to read his code and understand his thinking, and it makes me pretty confident that if I spend some effort reading some code, that I can understand what is happening. I was also able to, as we were troubleshooting, map out our existing logic on a small whiteboard, which was very helpful in visualizing the web of logic that we had, as well as what helping understand what kind of issues might arise.