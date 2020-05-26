# Dependency Injection

- A dependency is any object that another object requires.
- Code dependencies (such as the previous example) are problematic and should be avoided for the following reasons:
  - To replace MyDependency with a different implementation, the class must be modified.
  - If MyDependency has dependencies, they must be configured by the class. In a large project with multiple classes depending on MyDependency, the configuration code becomes scattered across the app.
  - This implementation is difficult to unit test. The app should use a mock or stub MyDependency class, which isn't possible with this approach.
- Dependency injection addresses these problems through:
  - The use of an interface or base class to abstract the dependency implementation.
  - Registration of the dependency in a service container. ASP.NET Core provides a built-in service container, IServiceProvider. Services are registered in the app's Startup.ConfigureServices method.
  - Injection of the service into the constructor of the class where it's used. The framework takes on the responsibility of creating an instance of the dependency and disposing of it when it's no longer needed.
- create an interface for your dependency and apply it to a concrete dependency class
