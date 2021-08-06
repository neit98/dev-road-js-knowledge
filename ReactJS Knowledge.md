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
