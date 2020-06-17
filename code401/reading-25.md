# React Testing and Deployment

**Testing** 
- Snapshots : Make assertions on the exact rendered markup (with content) at any state of the application.
- Render Testing : Similar to snapshots, but allows for jQuery-like inspection of the virtual DOM tree
- Shallow Testing : Executes and renders the called/container component, but does not compose children.
- Mounting : Executes the full component and children. Allows for inspection of rendered Virtual DOM as well as the current state

**Deployment**
- uses a node service to create a live website that refreshes as you write code, not what gets deployed in live site
- if you use `npm run build` it will export a condensed set of static pages.

**Running Tests with Jest**
- use it() or test() blocks
 ```
 it('sums numbers', () => {
  expect(sum(1, 2)).toEqual(3);
  expect(sum(2, 2)).toEqual(4);
});
 ```
 - can create a "smoke test" that verifies a component runs without throwing errors
 ```
 it('renders without crashing', () => {
  const div = document.createElement('div');
  ReactDOM.render(<App />, div);
});
 ```
 - shallow rendering is meant to test in isolation from child components that they render
   - requires rendering API from Enzyme `npm install --save enzyme enzyme-adapter-react-16 react-test-renderer`
   - config global setup file `configure({ adapter: new Adapter() });`
   - ```
       it('renders without crashing', () => {
       shallow(<App />);
       });
     ```