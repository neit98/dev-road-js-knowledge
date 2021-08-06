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
