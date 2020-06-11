Authentication and Authorization with JWT

- after the JWT is created, each following request will need the token to authorize access to pages and features
- this process can be simulated in postman
- using Post for creating a user or signing in Postman will give you the token in the body of the response
- Create a new environment, see the big red button, top left.
- then under the Test tab, save the access token as an environment variable with pm.environment.set()
- if you check the Quick Look icon, you can see the saved JWT
- you can send the token either in the header or as an authorization helper
- Header
  - Under the Headers tab, add a key called Authorization with the value `Bearer <your-jwt-token>`
  - use double curly brackets `{{}}` to swap in the token
  - header is displayed explicitly in the API documentation
- Authorization Helper
  - Under the Authorization tab, select the Bearer Token authorization type
  -  use double curly brackets `{{}}` to swap in the token
  - Can set authorization at the collection-, folder-, or request-level. Easy to set up the same authorization method for every request inside the collection or folder
  - Authorization is saved under the auth property
