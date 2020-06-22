# React Hooks

- React hooks allow to to easily create and manage state in a functional component.
- Hooks are JavaScript functions, but they impose additional rules
  - name must being with `use`
  - hooks can only be called at the "top" level, cannot be used inside loops, conditionals, or nested functions
  - Only call Hooks from React function components.
- built in example: `useState`
- Hooks allow you to reuse stateful logic without changing your component hierarchy.
- Hooks let you split one component into smaller functions based on what pieces are related (such as setting up a subscription or fetching data)
- Hooks are functions that let you “hook into” React state and lifecycle features from function components. Hooks don’t work inside classes — they let you use React without classes. 
- What is a Hook? A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.
- useState declares a kind of fuction state variable as a way to preserve information between function calls.
  - serves the same function as this.state for classes, only for functions!
  - can pass in a objected or just a number
  - returns a pair of values: the current state and a function that updates it
  - this is way they often use `const [count, setCount] = useState()`
- To display the prop use `{count}`
- to update `<button onClick={() => setCount(count + 1)}>`
- to have a function state with multiple props, simply use useState more than once
```
   function ExampleWithManyStates() {
  // Declare multiple state variables!
  const [age, setAge] = useState(42);
  const [fruit, setFruit] = useState('banana');
  const [todos, setTodos] = useState([{ text: 'Learn Hooks' }]);
```
- Examples of "side effects" or Effects are Data fetching, setting up a subscription, and manually changing the DOM in React components
- Network requests, manual DOM mutations, and logging are common examples of effects that don’t require a cleanup.
- example of useEffect
```
    useEffect(() => {
    document.title = `You clicked ${count} times`;
    });
```
- useEffect: tells the component needs to run the hook after it renders.
- placing useEffect inside a component gives it access to its state variables/props
- Effects with Cleanup
- For example, we might want to set up a subscription to some external data source. In that case, it is important to clean up so that we don’t introduce a memory leak! 
```
  useEffect(() => {
    function handleStatusChange(status) {
      setIsOnline(status.isOnline);
    }
    ChatAPI.subscribeToFriendStatus(props.friend.id, handleStatusChange);
    // Specify how to clean up after this effect:
    return function cleanup() {
      ChatAPI.unsubscribeFromFriendStatus(props.friend.id, handleStatusChange);
    };
  });
```