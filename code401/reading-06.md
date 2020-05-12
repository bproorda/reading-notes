# Interfaces

**Inheritance**
- Inheritance enables you to create new classes that reuse, extend, and modify the behavior defined in other classes
- *derived* classes inherits properites and behaviors from *base* classes
- a derived class is a specialization of the base class, animal -> mammal -> otter
- Interface declarations may define a default implementation for its members.
- derived class reuses the code in the base class without having to reimplement it. You can add more members in the derived class. The derived class extends the functionality of the base class.
- if a base class had a virtual method, it *can* be overriden by concrete derived classes
- an abstract method *must* be overriden in the derived class
- if the derived class is also abstract, it passes it along to the derived class
- if a class had abstract methods, the class must be declared abstract
- An interface is a reference type that defines a set of members
- Interfaces are used to define specific capabilities for classes that don't necessarily have an "is a" relationship
- if a class is labeled as sealed if prevents another class from inheriting it

**Abstract**
- the abstract keyword allows you to make incomplete classes that must be completed more specialized derived classes
- sealed keyword enables you to prevent the inheritance of a class
- to make class abstract: `public abstract class Name()`
- an abstract cannot be instantiated
- an abstract is a partial blueprint of common properties and behaviors of many different more specialized classes/objects
- abstract methods cannot be implented, they end with a semi-colon instead of code block.
  - the derived class *must* define the code block/behavior
- If a virtual method is declared abstract, it is still virtual to any class inheriting from the abstract class. 


**Polymorphism**
- Means many shapes in greek, describes how a single class can be used to create many different objects
- Virtual methods enable you to work with groups of related objects in a uniform way
- When a derived class inherits from a base class, it gains all the methods, fields, properties, and events of the base class
- A derived class can override a base class member only if the base class member is declared as virtual or abstract.
- Fields cannot be virtual; only methods, properties, events, and indexers can be virtual. 