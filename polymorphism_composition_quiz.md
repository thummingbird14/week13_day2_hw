# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean? It means "many forms"

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example. It means that we can treat an instance of a class as though it was another class / type at the same time. For example, if we have an instance of Printer where Printer implements IConnect, the printer is both a Printer and an IConnect at the same time.

3. What can we use to implement polymorphism in Java? Inheritance or (better) interfaces.

4. How many 'forms' can an object take when using polymorphism?
There's no restriction.

5. Give an example of when you could use polymorphism. If we wanted to connect a computer to a variety of devices (monitor, printet, speaker etc) we could create an IOutput interface and have Monitor implement IOutput, Printer implement IOutput and Speaker implement IOutput. Then the computer could have an output device which is an IOutput.



# Composition and Aggregation

6. What do we mean by 'composition' in reference to object-oriented programming? It is when an object is part of another object and cannot exist without it. It can be thought of as a "is part of" relationship.

7. When would you use composition? Provide a simple example in Java.
In the below example, House is composed of a Roof.
```
class Roof {
    private int width;
    private int length;
    private String type;

    ...
}

class House {
    private Roof roof;
    
    public House() {
        this.roof = new Roof();
    }
}
```



8. Give a difference between composition and aggregation?
In aggregation, objects can exist independently of the object which composes them. It can be thought of as a "has a" relationship.

9. What is/are the advantage(s) of using composition/aggregation?
It is flexible - behaviour of classes can be changed at run-time. Code can be reused. It allows for "multiple inheritance".

10. When using composition, when an object is destroyed, what happens to all the objects it is composed of? They are destroyed too.

11. When using aggregation, when an object is destroyed, what happens to all the objects it is composed of? They carry on existing.