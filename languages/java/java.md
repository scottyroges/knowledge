# Java

Static Class:
Only nested classes can be static

Static Method:
A class method that can be called even if there is no instance of that class
Rule of thumb: Would this method be useful even if there is no instance of the object? Does it use any instance variables?
ClassName.staticMethod();

Static Field:
All instances of the same class will be able to access this same field
The value is always the same between instances

Abstract Class:
A class that can not be instantiated
Define methods which can be used by the inheriting subclass.
Define abstract methods which the inheriting subclass must implement.
Provide a common interface which allows the subclass to be interchanged with all other subclasses.

Abstract Method:
If a class includes abstract methods, then the class itself must be declared abstract
a method that is declared without an implementation

Interface:
A reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. Method bodies exist only for default methods and static methods. Interfaces cannot be instantiated—they can only be implemented by classes or extended by other interfaces

Abstract Class vs Interface:
Consider using abstract classes if any of these statements apply to your situation:
You want to share code among several closely related classes.
You expect that classes that extend your abstract class have many common methods or fields, or require access modifiers other than public (such as protected and private).
You want to declare non-static or non-final fields. This enables you to define methods that can access and modify the state of the object to which they belong.
Consider using interfaces if any of these statements apply to your situation:
You expect that unrelated classes would implement your interface. For example, the interfaces Comparable and Cloneable are implemented by many unrelated classes.
You want to specify the behavior of a particular data type, but not concerned about who implements its behavior.
You want to take advantage of multiple inheritance of type.


Final Class
Cant be subclassed

Final Method
Cant be overridden

Final Field
Cant be changed

Anonymous Class

Inheritance
Class C = getClass(); 
while (C != null) { 
System.out.println(C.getName()); 
C = C.getSuperclass(); 
}

Serialization
The class must implement the java.io.Serializable interface.
All of the fields in the class must be serializable. If a field is not serializable, it must be marked transient.

Pass by Value

Singleton

Sort
java.util.Arrays.sort

BinarySearch
java.util.Arrays.binarySearch

String.valueOf
Integer.parse
string.toCharArray()
for loop iterator
