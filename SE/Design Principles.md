# Design Principles


Sure! Let’s go deep into each SOLID principle but still in simple, clear language, with examples so you truly understand.


---

S – Single Responsibility Principle (SRP)

Meaning: Every class or module should have one reason to change — in other words, it should do only one job.

Why important: If a class does too many things, changing one feature might break something else.

Example:

Bad: A class called Employee that handles both employee data and printing payslips.

Good:

Employee → stores employee info.

PayslipPrinter → handles printing payslips.



Key idea: Keep responsibilities separate so code is easier to maintain and debug.



---

O – Open/Closed Principle (OCP)

Meaning: Software entities (classes, modules, functions) should be open to extension but closed to modification.

Why important: Prevents breaking existing code when adding new features.

Example:

Bad: If you want to add a new type of shape to a drawing app, you modify the existing Shape class — this can introduce bugs.

Good: Use inheritance or interfaces:

Shape interface → implemented by Circle, Rectangle, Triangle.

Adding Hexagon → just create a new class implementing Shape, no need to change old code.



Key idea: Add new functionality without touching existing working code.



---

L – Liskov Substitution Principle (LSP)

Meaning: Objects of a child class should be able to replace objects of a parent class without affecting program behavior.

Why important: Ensures that derived classes are true substitutes for their base classes.

Example:

Bad:

class Bird { fly(); } 
class Ostrich extends Bird { fly(); } // Ostriches can’t fly → breaks program

Good:

class Bird { } 
class FlyingBird extends Bird { fly(); } 
class Ostrich extends Bird { }

Now, only birds that can fly use FlyingBird, no rules are broken.



Key idea: Derived classes should behave in a way that doesn’t surprise the program.



---

I – Interface Segregation Principle (ISP)

Meaning: Don’t force classes to implement methods they don’t need.

Why important: Prevents “fat” interfaces with unused methods, keeps code clean.

Example:

Bad: Interface Machine has print(), scan(), fax().

Printer class must implement scan() and fax() even if it can’t scan/fax.


Good: Split interfaces:

PrinterInterface → print()

ScannerInterface → scan()

FaxInterface → fax()



Key idea: Keep interfaces small and specific.



---

D – Dependency Inversion Principle (DIP)

Meaning:

1. High-level modules should not depend on low-level modules. Both should depend on abstractions (interfaces).


2. Abstractions should not depend on details; details should depend on abstractions.



Why important: Makes code flexible, easy to change, and easier to test.

Example:

Bad: Remote class directly uses TV class. If you change TV, Remote breaks.

Good:

interface Device { turnOn(); turnOff(); }
class TV implements Device { ... }
class Remote { Device device; }

Now Remote works with any device, not just TV.



Key idea: Depend on interfaces, not concrete classes.



---

If you want, I can also make a super easy visual diagram of SOLID principles with simple icons and examples so it sticks in your memory instantly.

Do you want me to make that?

