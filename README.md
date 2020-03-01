#OOP concepts
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

## Encapsulation
Encapsulation means wrapping up related data and mechanisms that manipulate the data under a single unit. 
- So one can think of class as an example of encapsulation, as a class holds all the related properties and methods in it. 
- It is also called data-hiding as the data in a class can be hidden from any outside code, by declaring all the variables in the       class as private and writing public methods in the class to set and get the values of variables.

## Abstarction
Data Abstraction is the property by virtue of which only the essential details are displayed to the user.The trivial or the non-essentials units are not displayed to the user. Ex: A car is viewed as a car rather than its individual components.
- In Java, abstarction can be achieved using Interfaces and Abstract Methods.

## Interfaces
Interfaces are refrence types similar to a class, it only consists of constants, method declarations i.e . abstract methods, default methods, static methods and nested types.
- Only static and default methods have method definations.
- Interfaces cannot be instantiated i.e. one cannot create an object from an Interface.
- All abstract, default, and static methods in an interface are implicitly public.
- All constant values defined in an interface are implicitly public, static, and final.

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
| Content Cell      | Content Cell  |
| Content Cell      | Content Cell  |



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

