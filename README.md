# My Project: Food Ordering app

Rough sketch of app
*Header
- logo
- Nav Items

*Body
- Search
- RestaurantContainer
   -restaurantcard
     - Img
     - Name of Restaurant, Star Ratings,quizine etc.

*Footer
- Copyright
-links
-address
-contact

******* Here we have same name of food card with same data in RestaurantCard, how we can dynamically change the data of the ReactComponent,so here the concept of props are coming. We can undestand this as a just normal  javascript arguments passing trough a function. i.e props (short for "properties") are like inputs we give to a React component to customize it. They allow you to pass data from a parent component to a child component.

**** Props is an Object


 *****Config Driven Ui: Controling the Ui using given data or given config is known as the config Driven UI,and config comes from the Backend.

 ***Our website is driven by the data ,that is known as config driven ui.

###Today's Learning : So when we want  dynamically passing few data to a component, we can pass it through the props, and we can pass any number of props we wish to.

@@@@ Two types of Export/import
1. Default Export/Import
export default Component;
import Component from "path"

2. Named Export/Import
export const Component;
import {component} from 'path';

<!-- When we use default export and named export? : when we have to export only one component then we use dafault export import but when we use multiple component to export , we use named export/import -->

Q. can we use  default and named export together in a code?
for ex:  export  const Header ={
  some piece of code
}
export default Header;

Ans: No, we cannot have both a named export and a default export for the same Header component in this way. This will cause an export conflict.

 ##State Variable in React: 
 In React, a state variable is a special variable used to store and manage dynamic data within a component. When the state changes, React automatically re-renders the component to reflect the new values. It is a super powerful variable. 

# Hooks in React:
 Hooks are special functions in React that allow functional components to manage state and side effects without needing class components. They were introduced in React 16.8 to simplify component logic and make code more reusable.

Common React Hooks: useState(),useEffect()

1. useState (Manages State in Functional Components):
Used to declare state variables inside functional components.

2. useEffect (Handles Side Effects):
Runs code after rendering, useful for data fetching, subscriptions, or manually updating the DOM.

<!-- Note: Whenever a state variable changes, react re-render its component -->

<!-- Virtual Dom : it is a representation of actual dom ,and actual doms are the tags(<div>,h1,h2) -->

# Reconciliation Algorithm in React:
In React 16 a new algorithm came out to update the Dom,which is known as Reconciliation ,and after react 16 it is known as "React Fiber" and React Fiber is the new way of finding the div and update the dom.

# Reconciliation:
 is the process of updating the UI efficiently when a component’s state or props change. Instead of re-rendering everything, React compares the previous Virtual DOM with the new Virtual DOM and updates only the changed parts in the real DOM.

🔹 Steps in Reconciliation:

1. React creates a new Virtual DOM after a state/prop change.
2. It compares the new Virtual DOM with the old one (Diffing Algorithm).
3. React identifies differences and updates only those elements in the real DOM.

# what is Diff Algorithm?
The Diff Algorithm is how React efficiently compares the new Virtual DOM with the old one to determine the minimal number of updates needed.

🔹 Key Optimizations in the Diff Algorithm:

🔹 Rule 1: Elements with Different Types Cause Full Re-Renders
If the element type changes, React destroys the old element and creates a new one.
✅ Example:

jsx
Copy
Edit
function App({ isTitle }) {
  return isTitle ? <h1>Title</h1> : <p>Paragraph</p>;
}
📌 If isTitle changes from true to false, React removes <h1> and creates <p>, instead of modifying <h1>.

🔹 Rule 2: Elements with the Same Type Get Updated in Place
If the element type remains the same, React updates only the changed attributes or text.
✅ Example:

jsx
Copy
Edit
function User({ name }) {
  return <h1>{name}</h1>;
}
📌 If name changes from "John" to "Doe", React only updates the text inside <h1>, not the entire element.