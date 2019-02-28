# Memento Design Pattern

# Is a behavioral design pattern that try to give a resolution to the issues with the backups
# and its recovery.
# To this design Memento lets you save and restore the previous state of an object
# with revealing the details of its implementation (Encapsulation), in this code example
# set a package called History where you can found two class:
# 1. Memento.class and History.class:
# Now this the conecction:
# Memento had two atrributes: backup and editor,
# Editor is our originator and had two atrributes canvas and history,
# Canvas had the possibles movements or changes in the color of the objects all the time is in mood Listeners to allow know the keyboards or mouse movements, 
# and History is an ArrayList<Pair> where Pair had <command, memento>
# Command is an Interface that implements two methods execute and getName (movement or color change)

# In this case the example allow us undo and redo, so, in this case the history is a list becasue if
# use pila or colas don't allow or redo or undo.

# the common issues with this design pattern is stablishment:
# 1. a tracking to the life cicle of the originator´s state to start to eliminate old states
# 2. to talk to a lot of states or objects, it needs more memory.