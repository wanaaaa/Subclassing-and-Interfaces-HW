---
title: Subclassing and Interfaces
type: Homework
duration: "1:00"
creator:
    name: Charlie Drews
    city: NYC
---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Subclassing, Abstract Classes, and Interfaces

> ***Note:*** _You can discuss with classmates, but everyone must submit their own answers_

## Exercise

#### Requirements

- Fork this repo, then add your answers direcly to this **readme.md** file
  - After forking, you can clone, edit the readme in the text editor of your choice, and push back to Github...
  - Or, you can edit the readme [right from the browser](https://help.github.com/articles/editing-files-in-your-repository/)
- After adding your answers, submit a **pull request**

#### Questions

1. What is the difference between *member variables* (also called *instance variables*) and *class variables* (w/ keyword `static`)? Which can be accessed without creating an instance of the class?

- Instance variables belong to an instance of a class. Class variables, however, only have one copy of the variable(s) shared with all instances of the class
- Class variable can be accessed without creating an instance of the class

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?
- Using public variable can cause setting wrong values to the variable as the input value cannot be checked.r 

3. What are some benefits of making member variables `private`?
- Other programer can not change it when they work together.

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?
- A: subclass, children
- B: superclass, parents

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?
- The method or variable goes from parent to children class.

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?
 - Becuase getTemperature is in Applicnace class, not in Refrigerator class.
 - Casting let a class use method in other class.

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?
- We can declare a method in normal class.However, abstract classes cannot be instantated directly. An abstract class  is one that does not provide implementations for all its methods. 


8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?
- An interface is a reference type in Java, it is similar to class, it is a collection of abstract methods.
- Interfaces cannot be instantiated, but rather are implemented.
- All of the methods in an interface are abstract.

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.
- We can not created an instance of an "abstract class."
- We cannot inherit final class , but abstract class can be inherit into subclasses. A method can never, ever, ever be marked as both abstract and final, or both abstract and private.


10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?
- The method which overrides other method is excuted. 
- The method in child is excuted 


11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?
- LinkedList and ArrayList is a child of List.
- When we use List rather than LinkedList of ArrayList, it can use some fetures which is only in List.

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/subclasses-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/interfaces-and-abstract-classes-lesson).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!
