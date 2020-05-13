# Interface 2
  - an interface is a set of properties/behavior, that a non abstract class must implement
  - interfaces allow applying data from multiple sources into a class
  - required to simulate inheritance for struct
  - interface name starts with I
  - Interfaces can contain instance methods, properties, events, indexers
  - Interfaces may contain static constructors, fields, constants, or operators.
  - when a class implements a interface it must define any properties and methods
  - Interfaces can inherit from one or more interfaces
  - An interface defines a contract. Any class or struct that implements that contract must provide an implementation of the members defined in the interface.
  - member declarations inside an interface do not need an implemenation, if they do it is the *default* implementation 
  - interface may not contain an instance state 
  -  When an interface overrides a method implemented in a base interface, it must use the explicit interface implementation syntax.
  