# MVC

- Model View Controller
  - architectual pattern that maintains separation of concerns by breaking an app into three parts
  - **Model**: Classes that make up data of the app. use validation logic to enforce business rules for that data. Typically, model objects retrieve and store model state in a database. 
  -  **View**: Views are the components that display the app's user interface (UI). Generally, this UI displays the model data.
  - **Controller**: Classes that handle browser requests. They retrieve model data and call view templates that return a response. In an MVC app, the view only displays information; the controller handles and responds to user input and interaction. For example, the controller handles route data and query-string values, and passes these values to the model. 
- Separation of Logic
  - The UI logic belongs in the view
  - Input logic belongs in the controller.
  - Business logic belongs in the model.
- Every public method in a controller is callable as an HTTP endpoint. In the sample above, both methods return a string. Note the comments preceding each method.
- `LocalHost:{PORT}/Class/Method/Parameters`
- runs index method if no method is specified
- ? is a url separator to signify query string, & to separate key value pairs
- with parameters, Use HtmlEncoder.Default.Encode to protect the app from malicious input (namely JavaScript).
- use Razor view files to cleanly encapsulate the process of generating HTML responses to a client.
- Razor-based view templates have a .cshtml file extension
- generally uses IActionResult