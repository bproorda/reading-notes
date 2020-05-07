# Classes & Objects
**Classes**
  - a class is reference type: when run a variable with reference type contains value null until an instance is created.
  - declared with class keyword `public class Customer`
  - a class defines a type of object but is not an object itself. an object is an entity based on a class, an instance
  - objects created with `new` keyword: `Customer object1 = new Customer();` 

**Constructor**
  - constructors allow the programmer to set defualt values,limit instantiation, etc
  - if you do not provide a constructor for your class, C# creates one.
  - the constructor has the same name as the name of its type, ie `public class Person` => `public Person(arguments)`
    - does not include a return type
  - Can also be static constructors that produce static members of type
    - contains no parameters
    - `static Person`
**Properties**
  - a member that provides a way to to read, write, or compute the value of a private field
   - a special kind of methods called *accessors*
  - gives a class a public mechanisim of getting and setting values, while hiding impementation or verification
  - a *get* property accessor is used to return the property value
  - a *set* property accessor is usedto assign a new value
  - !(screenshot)[property.png]