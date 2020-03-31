# OOP concepts - using Java
- **Polymorphism  - P**
- **Inheritance   - I**
- **Encapsulation - E**
- **Abstraction   - A**

## Polymorphism
Polymorphism refers to the ability of OOP language to differntiate between entities with same name. This can be achieved by signature and declaration of these entities.
- In Java, polymorphism can be achieved using method overloading and method overriding.
- In JavaScript, polymorphism can be achieved using method overriding. JavaScript supports overriding not overloading, meaning, that      if you define two functions with the same name, the last one defined will override the previously defined version and every time      a call will be made to the function, the last defined one will get executed.

## Inheritance
Inheritance is a mechanism by which an OOP language allows one class inherit properties and methods of another class and/or interface.
- The class and/or interface which is inherited is often called as Super, Parent, Base class.
- The class inheriting is called Child, Sub, Derived class.
- Is-A relation i.e. A car is a vehicle.

## Encapsulation
Encapsulation means wrapping up related data and mechanisms that manipulate the data under a single unit. 
- So one can think of class as an example of encapsulation, as a class holds all the related properties and methods in it. 
- It is also called data-hiding as the data in a class can be hidden from any outside code, by declaring all the variables in the       class as private and writing public methods in the class to set and get the values of variables.

## Abstraction
Data Abstraction is the property by virtue of which only the essential details are displayed to the user.The trivial or the non-essentials units are not displayed to the user. Ex: A car is viewed as a car rather than its individual components.
- In Java, abstarction can be achieved using Interfaces and Abstract Methods.

## Composition
It's a type of inheritance where classes are associated with other classes rather than actually inheriting them. It can be practically achieved by having other classes as properties of a certain class.
- It's a Has-A relation i.e. A car has an engine.

## Class
A class is a blueprint from which objects are created. It consists of related properties and methods.

```
class Person{

  private string fullName;
  
  public Person(string fullName){
    this.fullName = fullName;
  }
  
  public getFullName(){
  
    return this.fullName;
  
  }

}
```

## Object
Object is an instance of a class. Objects represents real life entities.
```
//Refer to code above
Person jon = new Person("Jon");
jon.getFullName();//Jon

Person jane = new Person("Jane");
jane.getFullName();//Jane
```

## Interfaces
Interfaces are refrence types similar to a class, it only consists of constants, method declarations i.e . abstract methods, default methods, static methods and nested types.
- Only static and default methods have method definations.
- Interfaces cannot be instantiated i.e. one cannot create an object from an Interface.
- All abstract, default, and static methods in an interface are implicitly public.
- All constant values defined in an interface are implicitly public, static, and final.
- Because ow Interfaces behave, they are also called as contracts.

## Abstract Classs
An abstract class is a class that is declared abstract—it may or may not include abstract methods. Abstract classes cannot be instantiated, but they can be subclassed i.e. inherited.

## Abstract Methods
An abstract method is a method that is declared without an implementation (without braces, and followed by a semicolon.
```
abstract void moveTo(double deltaX, double deltaY);
```
Abstract classes vs Interfaces

| Abstract classes  | Interfaces    |
| ----------------- | ------------- |
| Cannot be instantiated      | Cannot be instantiated |
| Can be extended      | Can be implmented  |
| Can declare fields that are not static and final      | All fields are automatically public, static, and final  |
| Can declare public, protected, and private concrete methods   | All methods that you declare or define (as default methods) are public  |
| In Java multiple inheritance is not allowed so, one can only extend one abstract class.  | One can implement any number of interfaces.  |

## Method Overloading
When two or more methods in a class have the same name but different parameters i.e. different number of parameters and/or different data types, then this phenomenon is called Method Overloading.

```
public class Sum { 
  
    // Overloaded sum(). This sum takes two int parameters 
    public int sum(int x, int y) 
    { 
        return (x + y); 
    } 
  
    // Overloaded sum(). This sum takes three int parameters 
    public int sum(int x, int y, int z) 
    { 
        return (x + y + z); 
    } 
  
    // Overloaded sum(). This sum takes two double parameters 
    public double sum(double x, double y) 
    { 
        return (x + y); 
    } 
  
    // Driver code 
    public static void main(String args[]) 
    { 
        Sum s = new Sum(); 
        System.out.println(s.sum(10, 20));
        //30
        System.out.println(s.sum(10, 20, 30)); 
        //60
        System.out.println(s.sum(10.5, 20.5)); 
        //31.0
    } 
}
```
## Method Overriding 
When a child class has a method with a same name and same parameters (number and data type - wise) as of its parent, then the method in the child class is said to override the method from the parent class.

```
class Parent { 
    void show() 
    { 
        System.out.println("Parent's show()"); 
    } 
} 
  
// Inherited class 
class Child extends Parent { 
    // This method overrides show() of Parent 
    @Override
    void show() 
    { 
        System.out.println("Child's show()"); 
    } 
} 
  
// Driver class 
class Main { 
    public static void main(String[] args) 
    { 
        // If a Parent type reference refers 
        // to a Parent object, then Parent's 
        // show is called 
        Parent obj1 = new Parent(); 
        obj1.show(); 
        //Parent's show()
  
        // If a Parent type reference refers 
        // to a Child object Child's show() 
        // is called. This is called RUN TIME 
        // POLYMORPHISM. 
        Parent obj2 = new Child(); 
        obj2.show();
        //Child's show()
    } 
}
```

## Constructor
Constructor are used to initialize the object's state i.e. properties.
- One can think of constructors as function/methods.
- Constructors are called when an object is initialized.
- In Java, contructors should have same name as of the class.
- In JavaScript, one can use keyword called constructor()

## Upcasting
Converting a derived class to the base class.

```
class Parent{
}

class Child{
}

Child jon = new Child();

Parent parentJon = (Parent) jon;

```

## Downcasting
Converting base class to derived class.
```
class Parent{
}

class Child{
}

Parent parentJon = new Child();

```

## Boxing or Autoboxing
Converting a primitive type into a corresponding Wrapper or Object is called Boxing. 
```
int no = 10;
Object objNo = no;
```

## Unboxing
Converting a object type into a primitive type is called Unboxing.
```
Object objNo = no;

int a = (int) objNo;
```

# JavaScript Basics & Advanced Concepts

## Inheritance in JavaScript
Unlike Java, JavaScript uses prototypical inheritance. In simple terms instead of classes inheriting from classes, in JavaScript its objects inheriting from object.

```
//This is a constructor function for Person object
//And we know that functions are also objects in JavaScript
//So this function is also an object
function Person(){
  //...
}
//Create a new object using the Person constructor
const circle = new Person();

const array = new Array();
 
```
In the snippet above, the object circle will be derived from prototype of the constructor function which further will be derived from the root object. Root object doesn't have a prototype. Lets consider the array object, it will be derived from a prototype (i.e. constructor function) of Array which further will be derived from root prototype.


## Abstraction in JavaScript
In JavaScript, inorder to make properties and methods of an object abstract, one must declare them as local entities (Refer to the code below). So basic idea is to not use 'this' while declaring any property or method, to make it abstract.
```
function Person(fname, lname){
  //These properties and methods can be accessed by using dot or bracket notations
  this.fname = fname;
  this.lname = lname;
  this.displayName = () => {
    console.log(fname + " " + lname);
  };
  
  //These properties and methods cannot be accessed by using dot or bracket notations
  //Hence these properties remain abstract or not reachable by outside world
  let firstName = "Jon";
  let lastName = "Doe";
  displayFullName = () => {
    console.log(fname + " " + lname);
  };
}
```


## Creating object in JavaScript
There are three ways using which one can create objects in JavaScript.
1. Using Object literal syntax.
```
const person = {
  fname: 'Jon',
  lname: 'Doe',
  walk: function() {
    console.log('Walking...');
  }
};

```
2. Using Factory function.
```
function createPerson(fname, lname){
  return {
    fname: fname,
    lname: lname,
    walk: function() {
      console.log('Walking...');
    }
  };
}
//Create an object
const jon = createPerson('Jon', 'Doe');
jon.walk()//Walking...

```
3. Using Constructor function.
```
function Person(fname, lname){
  this.fname = fname;
  this.lname = lname;
  
  this.walk = function(){
    console.log('Walking...');
  }
  
}

//Create an object
const jon = new Person("Jon","Doe");
jon.walk()//Walking...

```
When using the constructor function i.e. use new operator to create an object, three things happen in the following order.
1. It will create an empty object.
2. It will point 'this' to the object.
3. It will return the newly created object.

## Constructor property in JavaScript
In JavaScript, all objects have a property called constructor. It holds the function that was used in order to create the object.

## Value vs Refrence Types
In JavaScript, 
- Primimitives are copied by their value.
- Objects are copied by their refrence.

## Getter and Setters in JavaScript
```
function Person(){
  let firstName = "";
  
  Object.defineProperty(this, 'firstName', {
    get: function(){
      return firstName;
    },
    set: function(value){
      firstName = value;
    }
  });
  
}

const person = new Person();

person.firstName = "Jon";//Setter
person.firstName;//"Jon"//Getter

```












