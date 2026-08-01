# OOP Concepts

**Key points / formula:** Four pillars: Encapsulation (bundling data + methods, hiding internal state), Inheritance (a class reuses/extends another's behavior), Polymorphism (same interface, different implementations — compile-time via overloading, run-time via overriding), Abstraction (exposing only essential behavior, hiding implementation details via interfaces/abstract classes).

**When it's asked (pattern cue):** "Explain OOP pillars with real-world examples," or "difference between overloading and overriding," or "abstract class vs interface" — almost always the opening question in a domain round.

**Worked micro-example:** Polymorphism via method overriding.
```
class Animal { sound() { return "..."; } }
class Dog extends Animal { sound() { return "Bark"; } }
class Cat extends Animal { sound() { return "Meow"; } }
Animal a = new Dog(); a.sound() -> "Bark" (resolved at runtime)
```

**Common gotcha / trick:** Confusing overloading (same method name, different parameters, resolved at compile time) with overriding (subclass redefines a parent method, resolved at runtime); saying "abstract class and interface are the same" without noting the real distinction (multiple inheritance support, default implementations, state/fields).
