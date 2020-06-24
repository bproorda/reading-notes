# Context API
- Context provides a way to pass data through the component tree without having to pass props down manually at every level.
- provides a way to share values like locale preference, or UI theme between components without having to explicitly pass a prop through every level of the tree.
- Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.
```
// Context lets us pass a value deep into the component tree
// without explicitly threading it through every component.
// Create a context for the current theme (with "light" as the default).
const ThemeContext = React.createContext('light');

class App extends React.Component {
  render() {
    // Use a Provider to pass the current theme to the tree below.
    // Any component can read it, no matter how deep it is.
    // In this example, we're passing "dark" as the current value.
    return (
      <ThemeContext.Provider value="dark">
        <Toolbar />
      </ThemeContext.Provider>
    );
  }
}
```
- Apply context sparingly because it makes component reuse more difficult.
- If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.
- to create a context object `const MyContext = React.createContext(defaultValue);`
- when react renders a component it connected to the context it will read the current context value from the closest matching Provider above it in the tree.
- defaultValue argument is only used when a component does not have a matching Provider above it in the tree.
- passing undefined as a Provider value does not cause consuming components to use defaultValue
- context provider : `<MyContext.Provider value={/* some value */}>`