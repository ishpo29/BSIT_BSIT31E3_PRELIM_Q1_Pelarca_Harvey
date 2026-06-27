1. Why did you use inheritance?

I used inheritance because several classes such as Car, Boat, Airplane, and Helicopter share similar behavior. Instead of repeating code, these classes can inherit from a common parent class.
In this case, all these classes inherit from the abstract class Vehicle. The Vehicle class defines a shared method Move(), which is implemented differently by each child class.
Using inheritance expresses the idea that all these objects are types of vehicles (IS-A relationship).

2. Why did you use interfaces?
   
I used interfaces to define what an object is capable of doing. Interfaces act as a contract that specifies certain behaviors.
IFlyable means the object can fly
IDriveable means the object can drive
ISailable means the object can sail

If a class needs multiple abilities, it can implement multiple interfaces. This makes the design flexible and clearly shows each object’s capabilities (CAN-DO relationship).

3. Could Helicopter inherit from both Vehicle and Airplane? Why or why not?

No, a class in C# cannot inherit from more than one class.
Since Helicopter already inherits from Vehicle, it cannot also inherit from Airplane. C# only allows single inheritance for classes.
Even if it were possible, it would not make sense logically, because Helicopter and Airplane are both types of vehicles, not parent-child classes of each other.

4. Why can Helicopter implement both IFlyable and IDriveable?

Helicopter can implement both interfaces because interfaces are different from classes.
In C#, a class can implement multiple interfaces. This allows Helicopter to have both abilities:

It can fly (IFlyable)
It can drive (IDriveable)

This demonstrates how interfaces allow a class to support multiple behaviors.

5. If a Submarine can both sail and dive, how would you design it?

If a submarine can both sail and dive, I would design it similar to the Helicopter by implementing multiple interfaces.
The Submarine class would:

Inherit from Vehicle
Implement ISailable (can sail)
Implement another interface like IDiveable (can dive)

EXAMPLE:

namespace TransportChallenge;

public class Submarine : Vehicle, ISailable, IDriveable
{
    public override string Move()
    {
        return "Sailing in the water.";
    }
}

RESOLVER:

else if (input == "submarine")
{
    return new Submarine();
}
