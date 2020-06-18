# Component Composition

- Rounting
  - the coder can use react-router to toggle visibility for components/pages based on the url
  - `import { Route } from 'react-router-dom';`
  - `npm install --save react-router-dom`
  - requires replaces `<a>`tags with `<link>` tags
  - ```
      <Link to="/">Home</Link>
      <Link to="/stuff">Stuff</Link>
    ```
  - this is followed by the router component
   ```
    <Route exact path="/" component={Home} />
    <Route exact path="/stuff" render={() => <List>{items}</List>} />
   ```
  - based on the route, it will display the home or the items components

  - Router components only expect to receive a single child element. To work within this limitation, it is useful to create an <App> component that renders the rest of your application.
  - ```
       ReactDOM.render((
       <BrowserRouter>
       <App />
       </BrowserRouter>
       ), document.getElementById('root'));
    ```
  - if using `<Route path='/roster'/>` both `/roster` and `/roster/2` would match the route.
    - if the coder wants to make sure *only* `/roster` matches use an exact path, `<Route exact path='/roster'/>`
  - Routes can use one of three props to define what should render when the path matches
    - component: A react element.  When a route with a component prop matches, the route will return a new element whose type is the provided React component (created using React.createElement).
    - render: a function returning a react Element. This is similar to component, but is useful for inline rendering and passing extra props to the element.
    - children: A function that returns a React element. Unlike the prior two props, this will always be rendered, regardless of whether the route’s path matches the current location. not often used.
    ```
      <Route path='/page' component={Page} />
      const extraProps = { color: 'red' }
      <Route path='/page' render={(props) => (
      <Page {...props} data={extraProps}/>
       )}/>
      <Route path='/page' children={(props) => (
      props.match
       ? <Page {...props}/>
       : <EmptyPage {...props}/>
       )}/>
    ```
 - the main or app will have a switch element containing the routes
 - something like `/roster/:number ` would be handled by the `<roster>` component's switch, not be have its own route in the  main switch
   - uses a path param to capture the part of the pathname that comes after /roster.
   - the path param is noted by `:`
   ```
       function Roster() {
       return (
        <Switch>
         <Route exact path='/roster' component={FullRoster}/>
         <Route path='/roster/:number' component={Player}/>
        </Switch>
        );
        }
   ```
   - the param is passed as a prop and used by the player component
   ```
   // an API that returns a player object
   import PlayerAPI from './PlayerAPI'
    function Player(props) {
     const player = PlayerAPI.get(
      parseInt(props.match.params.number, 10)
      )
     if (!player) {
       return <div>Sorry, but the player was not found</div>
      }
      return (
       <div>
         <h1>{player.name} (#{player.number})</h1>
         <h2>{player.position}</h2>
       </div>
      );
     }
   ```


