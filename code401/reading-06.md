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
 