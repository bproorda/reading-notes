# Creating Custom React Hooks

- in addition to the build hooks, coder can create their own hooks to DRY up their applications
- anything that is a function can be a hook
- MUST have the prefix `use`
  - tells the program that this function follows hooks' rules
- code that is duplicated accross components or functions can be modularized into a hook
- a hook can call a hook
  - for example, your custom hook can call the `useEffect` hook.
```
  const useDocumentTitle = (title) => {
    useEffect(() => {
     document.title = title;
    }, [title])
  }
``` 
**Async Hooks**
  - async/await can be used with many hooks, DRY code!
  - async/await CANNOT be used with useEffect
  ```
  React.useEffect(() => {
    async function fetchBookList() {
      try {
        setLoading("true");
        const response = await fetch(
          `https://www.googleapis.com/books/v1/volumes?q=${searchBook}`
        );

        const json = await response.json();
        // console.log(json);
        setResult(
          json.items.map(item => {
            console.log(item.volumeInfo.title);
            return item.volumeInfo.title;
          })
        );
      } catch (error) {
        setLoading("null");
      }
    }

    if (searchBook !== "") {
      fetchBookList();
    }
  }, [searchBook]);
  ```
**useReducer Hook**
  - `const [state, dispatch] = useReducer(reducer, initialArg, init);`
  - alternative to useState
  - uses reducer of type (state, action ) => newState
  - useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one.
  - returns the current state paired with a dispatch method
  ```
  const initialState = {count: 0};

function reducer(state, action) {
  switch (action.type) {
    case 'increment':
      return {count: state.count + 1};
    case 'decrement':
      return {count: state.count - 1};
    default:
      throw new Error();
  }
}

function Counter() {
  const [state, dispatch] = useReducer(reducer, initialState);
  return (
    <>
      Count: {state.count}
      <button onClick={() => dispatch({type: 'decrement'})}>-</button>
      <button onClick={() => dispatch({type: 'increment'})}>+</button>
    </>
  );
}
  ```
  - to initialize useReducer
    - pass in intial state as argument 
      ```
        const [state, dispatch] = useReducer(
          reducer,
          {count: initialCount}
        );
      ```
    - or pass in an init function
    ```
       function init(initialCount) {
         return {count: initialCount};
        }
        const [state, dispatch] = useReducer(reducer, initialCount, init);
    ```
  - If you return the same value from a Reducer Hook as the current state, React will bail out without rendering the children or firing effects.
**10 hooks you should know**
https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d