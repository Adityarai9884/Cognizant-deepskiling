design Patterns & Principles

Part 1 — SOLID Principles
Think of SOLID as 5 rules for writing clean code. Interviewers and MCQs LOVE these.

S — Single Responsibility Principle (SRP)

One class should do ONE job only.

Bad example — a class that both calculates salary AND sends email. That's 2 jobs.

Good example — SalaryCalculator class only calculates. EmailSender class only sends email.

O — Open/Closed Principle (OCP)

A class should be OPEN for extension but CLOSED for modification.

Meaning — if you want new behaviour, ADD new code, don't EDIT old working code. This prevents breaking existing features.

L — Liskov Substitution Principle (LSP)

A child class should be able to REPLACE its parent class without breaking anything.

If Bird has a fly() method, and Penguin extends Bird — this breaks LSP because penguins can't fly. Bad design!

I — Interface Segregation Principle (ISP)

Don't force a class to implement methods it doesn't need.

Instead of one fat interface with 10 methods, make smaller focused interfaces.

D — Dependency Inversion Principle (DIP)

High level classes should NOT depend on low level classes. Both should depend on interfaces.




Design Patterns (The Famous GoF Patterns)
There are 3 categories — Creational, Structural, Behavioral. For your MCQ, focus on these 6:

CREATIONAL — how objects are created
1. Singleton Pattern

Only ONE instance of a class exists throughout the program.

Real life example — your printer spooler, database connection pool.

code:
class Singleton {
    private static Singleton instance;
    private Singleton() {}  // private constructor!
    
    public static Singleton getInstance() {
        if (instance == null)
            instance = new Singleton();
        return instance;
    }
}




2. Factory Pattern

Instead of using new directly, a factory method decides which object to create.

Real life — a vehicle factory that creates Car or Bike based on input.
3. Builder Pattern

Used when object creation has many optional steps.

Real life — building a burger (with/without cheese, with/without sauce etc.)



STRUCTURAL — how classes are connected
4. Adapter Pattern

Makes two incompatible interfaces work together.

Real life — your phone charger adapter (converts one plug type to another).
5. Decorator Pattern

Adds extra features to an object without changing its class.

Real life — coffee with milk, coffee with sugar — you're decorating the base coffee.


BEHAVIORAL — how objects communicate
6. Observer Pattern

When one object changes, all its dependents get notified automatically.

Real life — YouTube notifications. You subscribe (observe) a channel, you get notified when new video drops.