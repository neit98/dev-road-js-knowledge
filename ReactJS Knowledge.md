### State and Props
- **props** (short for “properties”) and **state** are both plain JavaScript objects. While both hold information that influences the output of render, they are different in one important way: **props** get passed to the component (similar to function parameters) whereas **state** is managed within the component (similar to variables declared within a function).
- while **props** and **state** both hold information relating to the component, they are used differently and should be kept separate.
- **props** contains information set by the parent component (although defaults can be set) and should not be changed.
- **state** contains 'private' information for the component to initial, change, and use on it's own.
- **props** are a way of passing data from parent to child, **state** is reserved only for interactivity, data that changes over time.

- both **props** and **state** are plain js objects.
- both **props** and **state** changes trigger a render update.
- both **props** and **state** are deterministic.

|   | **props**  | **state** |
| :------------ |:---------------:| -----:|
| Can get initial value from parent Component? | Yes | Yes |
| Can be changed by parent Component? | Yes | No |
| Can set default values inside Components? | Yes | Yes |
| Can change inside Component | No | Yes |
| Can set initial value for child comp ? | Yes | Yes |
| Can change in child comp ? | Yes | No |

-------------
### useLayoutEffect
- useEffect will run after render comp.
- useLayoutEffect will run before update UI.
- should use useLayoutEffect when have issue loading in DOM.

-------------
### func comp vs class comp
- func comp will re-render when parent comp re-render
#### Purpose of react hooks

* no **super** (props)
* no **this**
* maintain & look code easier
* custom hooks

| **props**  | **state** |
|:---------------:| -----:|
|A func comp is just a plain js func that accepts props as an argument and returns a React element.|A class comp requires u to extend from React.Comp and create a render func which returns a React element.
|No render method used in func comp|Must have the render() method returning html.|
|stateless comp => accept data & display|stateful comp => imp logic & state|
|Don't have React lifecycle method => react hooks help func comp have lifecycle.|Have React lifecycle methods.|

-------------
### major features of ReactJS

#### The major features of React are:

* It uses **VirtualDom** instead of RealDom considering that RealDOM manipulations are expensive.
* Supports server-side rendering.
* Follows Unidirectional data flow or data binding.
* Uses reusable/composable UI components to develop the view.

-------------
### redux
- The state in redux is stored in memory. This means that, if u refresh the page the state gets wiped out. The state in redux just a variable that persists in memory because it is referenced by all redux functions
- Difference between state management and state persistence. Lib like Redux and Vuex usually keep track of your variables and provide tools for changing state (reducers, specifically) - but they dont manage the persistence of that state. Persistence refers to saving the state somewhere to reload it the next time someone comes to your app.
- Persistence is usually coded by hand (send the state to an API endpoint which saves it to a database, then when you reload the page you ping a different API endpoint to retrieve the state) or you utilize a plugin / module for your state manager to handle persistence for you. Like Redux Local Storage  
-------------
### BrowserRouter vs HashRouter
- **BrowserRouter**: uses historyAPI. Client-side React app is able to maintain clean routes like example.com/react/route but needs to be backed by web server. Usually this means that web server should be configured for single-page application. On client side, window.loction.pathname is aprsed by React router. React router renders a component that it was configured to render for /react/router.
- Additionally, the setup may involve server-side rendering, index.html may contain rendered components or data that are specific to current route.
- **Hash Router**: it uses URL hash, it puts no limitations on supported browser or web server. Server-side routing is independent from client-side routing.
- Backward-compatible single-page app can use it as example.com/#/react/route. The setup cannot be backed by server-side rendering because it's / path that is served on server side, #react/route URL hash cannot be read from server side. On client side, window.location.hash is parsed by React router. React router renders a component that it was configured to render for /react/route, similarly to BrowserRouter.
- Most importantly, HashRouter use cases aren't limited to SPA. A website may have legacy or search engine-friendly server-side routing, while React application may be a widget that maintains its state in URL like example.com/server/side/route#/react/route. Some page that contains React application is served on server side for /server/side/route, then on client side React router renders a component that it was configured to render for /react/route, similarly to previous scenario. 
-------------
### 