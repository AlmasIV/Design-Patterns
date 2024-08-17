# Memento Behavioral Pattern

This pattern lets you save the state of an object and then possibly recreate that state.

## Implementation Details

One way to implement this pattern is:

1. The **Originator** class is the class whose state must be remembered. Inside this class, declare the **Memento** class (as an internal class). Don't make this class public.
2. The **Memento** class must mirror the **Originator**'s properties. It is recommended to make the **Memento**'s state read-only.
3. Define a constructor that accepts an **Originator** instance and copies its properties.
4. Define a method that returns the **Memento** instance inside the **Originator** class. So only the **Originator** can create instances of the **Memento**.
5. Define a second method that will accept a **Memento** instance and set the corresponding properties. This will recreate the state.
6. The **Caretaker** class is the class that safely stores the **Memento** instances. Define a **Caretaker** class.
7. The **Caretaker** cannot analyze or change the state of the **Memento**s. Only some metadata, such as creation time, name and so on, can be available.

## Pros

1. You essentially created a roll-backing mechanism.

## Cons

1. Consumption of the memory might be high if you save a lot of **Memento** instances.
2. The implementation in some programming languages that doesn't support the nested classes functionality might violate the encapsulation.
3. The **Caretaker** needs to track obsolete state somehow. You need to implement this functionality.
