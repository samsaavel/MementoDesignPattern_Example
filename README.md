# Memento Design Pattern

Is a behavioral design pattern that try to give a resolution to the issues with the backups and its recovery.
To this design Memento lets you save and restore the previous state of an object without revealing the details of its implementation (Encapsulation), all the time should be keep the object's structure.
We have two options to implement:

## Diagram:
Use Encapsulation and is a common implementation in Java
![alt text](https://github.com/samsaavel/MementoDesignPattern_Example/blob/master/images/Capture.PNG)

## Diagram 2:
The encapsulation is more resctricted.
![alt text](https://github.com/samsaavel/MementoDesignPattern_Example/blob/master/images/Capture1.PNG)

## Code
To understand this example, start with the set a package called History where you can found two class:
Memento.class and History.class
 Memento has two atrributes: backup and editor, Editor is our originator and has two atrributes canvas and history, Canvas has the possibles movements or changes in the color of the objects, all the time is in state Listeners to allow know the changes keyboards or mouse movements, and History is an ArrayList<Pair> where Pair had <command, memento>. Command is an Interface that implements two methods: execute and getName (movement or color change).
In this case the example allow us undo and redo, so, in this case the history is a list becasue use pila or colas don't allow redo or undo.

## Advantage
1. Generate the copies with the generator, it allow us a full copies.
2. Keep a complete history in the changes of object's state.

## Disadvantage
The common issues with this design pattern is stablishment:
1. Is need keep a tracking to the life cicle of the originator´s state to start to eliminate old states.
2. A lot of states or objects, it needs more memory.