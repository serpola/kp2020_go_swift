# Compare Object Oriented Programming in Go with Swift
## Serdar Polat

## Table of Contents
1. [Introduction](#1.Introduction)

2. [Concept of OOP](# 2.Concept of Object Oriented Programming)

2.1 [Concept](# 2.1Concept)

2.2 [Characteristics](# 2.2Characteristics)

3. [Golang](# 3.Golang)

4. [Swift](# 4.Swift)

5. [Conclusion](# 5.Conclusion)

# 1.Introduction
Meanwhile there are many different programming languages. These differ in their concepts. Depending on what is to be implemented, one of them is used. For example, there are concepts of distributed programming, functional programming or object-oriented programming. This paper compares the concepts of object-oriented programming in the programming languages GO and Swift.

The following chapter explains the concept of object-oriented programming in general. It then goes on to explain the basics of this object-oriented programming, how it can be depicted in diagrams and what the most important features of this are.

In the following two chapters, the concept of object-oriented programming in Go and Swift is explained. Here, the features explained in chapter 2 are used as a guide.

In the last chapter of this thesis, the differences between the programming languages Go and Swift are explained in relation to object-oriented programming.

# 2.Koncept of Object Oriented Programming
## 2.1Concept
Object-oriented programming is a programming paradigm of imperative programming. By encapsulating data and code in objects, the problem to be solved is worked out step by step. With OOP, a higher degree of abstraction is thus achieved through modularisation into objects than, for example, through a procedural programming language. Because of the encapsulation, the objects can be checked and tested independently of other parts of the programme. By encapsulating the variables in the objects, they can only be changed by the respective methods. This ensures that the variables of the object are not influenced by other parts of the programme.

Object-oriented programming not only saves time because the code does not have to be written and adapted repeatedly, it also avoids copy-and-paste errors that occur during adaptation. Above all, through the inheritance of class-based languages, the basic code does not change through the original class and this makes it easier to implement new classes more quickly. Additionally it avoids to rewrite already existing methods a second time.

## 2.2Characteristics
### Objects
Objects have attributes that have a certain state at a certain time. The state of the variables can be changed by methods to obtain expected values for the object.
### Classes
Classes are the blueprint for the objects. They are used to manage similar objects such as a car. Cars have the same characteristics, but their properties such as make, colour, model or age can be different. Thus, the class would be the blueprint for objects of cars.
### Inheritance
Objects and classes share common properties in object-oriented programming according to the concept of inheritance. Superclasses inherit the properties they possess to subclasses. For example, a car is the subclass of vehicles, whereas a motorbike is also a subclass of vehicles. Since vehicles share properties such as colour, brand or mileage. This also additionally reduces the programming effort. For example, methods for determining the kilometre reading can already be implemented in the superclass Vehicle and do not have to be implemented again in the subclass.  [] 
### Polymorphism
Thanks to polymorphisation, methods can be overwritten. This means that in subclasses, methods with the same names of the superclass can be adapted specifically to the subclass. In addition, polymorphism allows object variables of the superclass to take on the object variables of the subclass. 
### Generalization
In object-oriented programming, generalisation is used to bundle classes and objects with common properties and methods into one logical unit.

# 3. Golang
Go lang is a open source Programming langue developed by Google and other contributors from the open source community. It was published in 2009. Go is a multi-paradigm language, which means it is imperative and declarative. Important in the conception of this language was that the memory is managed automatically, fast compilation is possible and native support for concurrent, system-oriented programming is possible. 
## 3.1 Classes
Go does not use classes for the implementation of object orchestration. Instead, it uses structures.
A structure contains a collection of elements. This is a type declaration. Structures can also be nested to represent more complex models.
```
type quadrat struct{

LaW int

}

```

## 3.2 Methods
Methods are implemented with the definite ```func```. The call is similar to classes, only called via the structur.
Methods are implemented with the definition ```func```. The call is similar to classes, only called via the structures.
```
Func ( q qudrat) Area () int{
Return q.LaW * q.LaW
}

func main() {
  q := quadrat{2}
  fmt.Println(q.Area())
}

```
## 3.3 Inheritance
Inheritance is solved in Go by embedding. Here, the structure of another structure is passed on, so that the "subclass" can execute the methods implemented for the "superclass".

```
type Person structur{
Name string
Alter int
}
type Student structur {
Person
martikelnummer int
} 
func (p Person)setName(){
//…
}
func main() {
  p := &Person{Name:"Max"}
  s := &Student{p}

  p.setName()
  s.setName()
}


```

## 3.4 Polymorphism

Virtual methods can be created through the Go interface. This means that a method can be implemented by different structures. Polymorphism is thus supported in Go.
Instead of a square, one could also calculate the area with a rectangle. The code would then look like this:

```
type calculation interface{
Area() int
}

func ( q qurat) Area() in {
Return  q.LaW * q.LaW

}
func ( r Rectangle) Area() int {
Return  r.length * r.wide
}
```

# 4.Swift
## 4.1 Classes

Swift offers classes for in comparison to Go. In addition, Swift also supports structures like GO. The most important similarities are that you can define properties for storing values and methods for providing functions. The biggest difference is that structures do not support inheritance like classes do. The coding for the implementation looks like this:
```

//structur 
struct Person{
var name: String
var age = 0
}

//class
class Rectangle{

var width = 0
var lenth = 0

}
```
The creation of instances looks like this:

```
let p = Person()
let rec = Rectangle()
```
## 4.2 Methods
Methods are implemented with the definition func. The call is the same for classes and structures.
```
class Calculation{
var result = 0.

func addition(byA a: Int, byB b: Int ){
result = a + b
}
}

//Using

let cal = Calculation

cal.addition(byA: 1, byB: 2 )

//result is now 3.
```

## 4.3 Inheritance

Inheritance is not very different in concept from other programming languages that provide inheritance. You inherit all the properties and methods of the superclass and Swift also offers overwriting of the methods.
The syntax for inheritance looks like this:
```
class Vehicle {
    var totaldriven = 0.0
    var description: String {
        return "the vehicle past \(totaldriven) kilometers"
    }
    func makeSound() {
        // do nothing
    }
}

//Inheritance
class Car: Vehicle {
    //...
}

```

## 4.4 Polymorphism

Swift Supports polymorphism. The Coding therefore looks like:

```
class Vehicle {
    var totaldriven = 0.0
    var description: String {
        return "the vehicle past \(totaldriven) kilometers"
    }
    func makeSound() {
        // do nothing
    }
}

//Inheritance
class Car: Vehicle {
//...
    override func makeSound() {
        // play motor sound
    }
}

class Cycle: Vehicle {
//...
    override func makeSound() {
        // mke no Sound
    }
}
```

# 5.Conclusion

Structures can be used to define types in Go in order to programme in an object-oriented manner. Classes are not needed for the implementation of objects. Inheritance in Go is achieved by embedding one or more structures in an inheriting structure. The methods of the structures can be used for other structures by embedding them. In addition, Go uses polymorphism and avoids complex type hierarchies.

Compared to Go, Swift offers additional class implementations for object-oriented programming. Inheritance is thus also offered here. Methods can be called by instances of classes as well as structures. Polymorphism is also offered in Swift.

The big difference is that Go does not offer classes and inheritance.


# Literature
https://www.inztitut.de/blog/glossar/objekte/
https://golang.org/doc/
https://www.innoq.com/de/blog/golang-grundlagen/
https://swift.org/documentation/
https://code.tutsplus.com/tutorials/swift-from-scratch-an-introduction-to-classes-and-structures--cms-23197
https://www.raywenderlich.com/599-object-oriented-programming-in-swift
