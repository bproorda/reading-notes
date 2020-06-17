# Props and state

- props are saved parameters/arguments for a component.
- props are passed into a component with a syntax that looks like HTML attributes. These are the equivalent of function params.
-  inputs are stateful child components. This means that we must manage the state of inputs through our own stateful component and one way data binding.
- the parent component manages the state for all child components of the form and passes any necessary state down into it’s inputs through the use of props
- each input has onchange event
- props is the name of the object passed into a component constructor and any prop added to a component in the JSX will be accessible as a property on props
  - must be passed in using the constructor's super function
- props can be data or methods
- State can only be passed from parent component to a child component through the use of props. This enforces the idea of one way data flow.