# *Classes:*
```
        It is a set of object which shares common characterstics/behaviour and commomn properties/attributes.
        It is not a real world entity. It's a template or a blueprint or a prototype from which objects are created.
        It doesn't occupy any memory.
        It is a group of variables of different data types and a group of methods.
```
        A class in Java can contain:
            data member
            method
            constructor
            nested class
            interface

        Syntax to create a class:
``` java
            class Student 
            {
                String name;                            // data member (also, instance variable)
                int age;                                // data member (also, instance variable)
            }

            public static void main(String args[])
            {
                Student student1 = new Student();       // creating an object of Student           
                student1.name = "Tushar";               // Assigning the value to the data member (name)
                student1.age = 19;                      // Assigning the value to the data member (age)
            }   
```
        Class declaration contains:
```
            Modifiers:
                A class can be public or has default access

            Class keyword:
                Used to create  a class 

            Class name:
                    Should begin with an initial letter(capitalized by convention)

            Superclass(if any):
                The name of the class's parent, if any, preceded by the keyword extends. 
                A class can only extend one parent.

            Interface(if any):
                A comma seperated list of interfaces implemented by the class, if any, preceded by the keyword implements.
                A class can implement multiple interfaces.

            Body:
                The class body is surrounded by braces{}.

            Constructors:
                Used for initiallizing new objects.

            Fields: 
                Variables that provide the state of the class and it's objects and methods are used to implement thebehavior of its objects.
```
# *Objects*:
```
        Its a basic unit of Object Oriented Programming and represents real-life entities.
        A typical Java creates many objects, which interact by invoking methods.
```
        An object consists of:
```
            State:
                Represented by attributes of an object.
                Reflects the properties of an objecct.
            Behavior:
                Represented by the methodsof an object..
                Reflects the response of an object with other objects.
            Identity:
                Gives a unique name to an object and enables one objevt to interact with other objects.
```
        
# *Declaring Objects (also known as Instantiating a Class):*
```
        When an object is  created, the class is said to be instantiated.
        All the instances share the attributes and the behavior of the class.
        But the values of those attributes are unique for each object.
        A single class may have any number of instances.
```

# *Initializing an Object:*
```
        The "new" operator instantiates a class by allocating memory for a new object and returning a reference to that memory.
        The "new" operator also invokes the class constructor.
```


# *Ways to create an Object of a Class:*
```
        Using "new" keyword:
            It's the most common and general way to create an object in Java.
```
                Syntax:
``` java
                    Test t = new Test();
```
```
        Using Class.forName(String className) method:
            There's a predefined class in java language package with name Class.
            The forName(String className) method returns the Class object associated with the class with the given sting name.
            On clalling newInstance() method on this Class object returns new instance of the class with the given string name.
```
            Example:
``` java
                // creating object of public class Test
                // consider class Test present in com.p1 package
                Test obj = (Test)Class.forName("com.p1.Test").newInstance();
```
```     
        Using clone() method:
            It is present in the Object class.
            It creates and returns a copy of the object.
```
``` java
                // creating object of class Test
                Test t1 = new Test();

                // creating a clone of the above object
                Test t2 = (Test)t1.clone();
```
# *Anonymous Objects:*
```
            The objects that are instantiated but are not stored in a reference variable.
            They are used for immediate method calls.
            They will be destroyed after method calling
            They are widely used in different libraries.
```