# Part-Project
PART 4B. 
Make the Part in Part.java an abstract type, and remove the implementation of the Part.fail() method.
NEW: Add a new private final instance variable to the ConsumablePart called USES, which will hold the number of uses the ConsumablePart starts with.
Add a check for non-string values to the constructors and setters of the Part class.  If the constructor notices a non-string, it should throw an IllegalArgumentException.
This may require other changes, because of the new throw statement?  Can you see where or why?  (Chapter 11)
What defines a "correct" input?
Name or Number:  Name can be anything of type String
NCAGE: Any 5 character String (numbers or letters).  Theoretically, it can't have any special characters, but we'll get to that when we start doing regular expressions in Chapter 14 or 15.
NIIN:  Must be of the form NNNN-NN-NNN-NNNN.  So for now, ensure that it's a String, and that it is 16 in length.  We'll worry about the hyphen pattern with regular expressions later. 
Make the required changes to PartTest.java to handle the Part objects polymorphicly.
Instead of instantiating Part objects, start creating ExpendableParts and ConsumableParts.  If this requires you to create Constructor methods for these two classes, do so in their respective classes.
Add an instance variable to the ExpendablePart called toolsRequired, which is an ArrayList of Consumble parts.
Modify the ExpendablePart by adding a public void addTool() method that takes a ConsumbablePart and adds it to the toolsRequired instance variable.
Modify the ExpendablePart.fail() method to call the ConsumablePart.fail() method for each Consumable Part in its toolsRequired ArrayList.
Modify the ConsumablePart.fail() method.  It now decrements the number of uses left for that part, but if the new number of uses isn't zero, it will not mention a cost to replace in the message.  However, if the new number of uses is now zero, ensure that the cost to replace the ConsumablePart is in the fail method's message, and then reset the number of uses to USES.
Examples of failure messages
Consumable Part XXXX has been used, and now has Y uses left.
Consumable Part WWWW has been used up, and will cost D.DD to replace.
Modify PartTest.java to run through the new functionality of the various Parts
Make a variable called system that is an ArrayList of ExpendablePart
