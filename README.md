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

<!-- State Variable in React: In React, a state variable is a special variable used to store and manage dynamic data within a component. When the state changes, React automatically re-renders the component to reflect the new values. -->