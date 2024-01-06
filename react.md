Q1 : What is React ? 
Ans : 1 : React is used to manipulate the DOM virtually without directly working on the actual dom so that it won't make DOM slow and make it cheaper to use.
1.2 : In react we make the element using React.createElement("div" , {className, id , children}) or 
      we can write it like    React.createElement("div" , 
                                          [ React.createElement("div",style{})],
                                          [ React.createElement("p"), className]
      )
1.3 : In vanilla javaScript we use the append or appendChild and in react we use render 
1.4 : React make a virtual Dom 
1.5 : During console.log we can see unfamiliar React elements for example : $$typeOf


Q2 : Who made React ? 
Ans : React was create by Facebook now called as meta , Father of React is Jorden Walke

Q3 : What is Babel ?
Ans : Babel in simple terms can be called as translator which work for browser to under the language of JSX 

Q4 : How does Babel convert html code in React into valid code ?
Ans : JSX : let element = <div>Carpe diem </div> 
 so here we can see half js let element and half "<div>Carpe diem </div>" html so togehter it is called JSX 
 this language browser can't understand hence babel helps to translate this to browser 
 
 jsx : let element = <div>Carpe diem </div>  browser
                        ^
                        |
                        |
                      babel
                        |
                        |
browserjs:      let element = /*#__Pure__*/React.createElement("div",null,"Carpe diem")

Q5 : What is ReactDOM used for? Write an example?
Ans : After learning about Ract.createElement we see that a new word react dom comes to play it key role , 
 here ReactDOM is something which work as a bridge between ReactElement and actual DOM , here it takes react element and convert it into actual dom and render or show it on the web page 


Example : 

let rootReact = ReactDOM.createRoot(rootElement)
rootReact.render(element)


Q6 : What are the packages that you need to import for react to work with ?
Ans : React package : https://www.unpkg.com/react@18.2.0/umd/react.development.js

React DOM package : https://www.unpkg.com/react-dom@18.2.0/umd/react-dom.development.js

other like can add babel using text/babel

Q7 : How do you add react to a web application ? 
Ans : STEP1 : Add a DOM container in HTML 
      <!-- Existing html -->
      <div id = "root"></div>  
      <!-- Existing html -->

      STEP2 : Add the Script Tag
    <script src = "https://www.unpkg.com/react@18.2.0/umd/react.development.js"></script>
    
    <script src = "https://www.unpkg.com/react-dom@18.2.0/umd/react-dom.development.js"></script>
    
    <script src="like_button.js"></script>

      STEP3 : Create a React Component 
    const domContainer = document.querySelector('#root');
    
    const rootReact = ReactDOM.createRoot(domContainer);
    
    rootReact.render(element , (LikeButton));


Q8 : What is React.createElement?
Ans : `React.createElement` is a function provided by React that is used to create React elements. It is the fundamental building block of React applications.

Here's an example of how `React.createElement` is used:

```jsx
const element = React.createElement('h1', { className: 'greeting' }, 'Hello, World!');
```

In this example, `React.createElement` is used to create a React element representing an `<h1>` heading with the class name "greeting" and the text content "Hello, World!". The first argument of `React.createElement` is the type of the element (in this case, `'h1'`), followed by an optional object of attributes or props, and finally the children of the element.

The `React.createElement` function returns a plain JavaScript object that represents the React element. This object can then be rendered to the DOM using `ReactDOM.render` or used as a component in a React application.



Q9 : What are the three properties that createElement accept?
Ans : The 3 properties that createElement accept 
  1 -> type // h1 , div , p 
  2 -> props // style 
  3 -> children 

Q10 :  What is the meaning of render and root?
Ans : In the context of React, "render" refers to the process of taking a React element or a component and displaying it on the screen or in the DOM (Document Object Model). The rendering process involves converting the React elements into actual HTML elements that can be seen and interacted with by users.

The "root" typically refers to the top-level element in the DOM where your React application is mounted. It serves as the entry point for your React component hierarchy. When you render your React application, you specify the root element where the application will be injected and rendered.

For example, in a typical React application, you might have the following code to render your app:
```jsx
ReactDOM.render(<App />, document.getElementById('root'));
```
In this example, `document.getElementById('root')` is the root element where the React application will be rendered. The React component `<App />` will be mounted and rendered inside this root element.

By specifying the root element, you can control where your React application appears on the webpage or within a specific part of your web application.


