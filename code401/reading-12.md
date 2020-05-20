# Effective Framework Core

  - EF Core can serve as an object-relational mapper (O/RM), enabling .NET developers to work with a database using .NET objects, and eliminating the need for most of the data-access code they usually need to write.
  - uses a model to access data
    - A model is made up of entity classes and a context object that represents a session with the database, allowing you to query and save data
  - Instances of your entity classes are retrieved from the database using LINQ
  - Data is created, deleted, and modified in the database using instances of your entity classes

# User Secrets
  -  User secrets is a secure way of storing private user information such as API keys, client secrets, and connection strings
  - to enable user secrets, right click on the project and manage enable user secrets
  - this creates a json document with key/value pairs
  - file is located at `%APPDATA%\microsoft\UserSecrets\<userSecretsId>\secrets.json`
  - open `.csproj` file
 - you should have a user secret ID line added in the propertyGroup section.
