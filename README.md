# Part-Project

Part 4a
Add a public method to Part called fail() that will print out a generic failure message, identifying the part that has failed.  fail() should return void.  Add a comment to the Part.fail() method that mentions that this method will be abstract at some point soon.

Extend class Part with two classes in accordance with the descriptions below:

ExpendablePart
add a private instance variable of type int called failureRate, which will hold the average number of failures per operational hour of the part.
add a private instance variable of the type int called leadTime, which will hold the number of days it takes to replace the part in the supply system.
ConsumablePart (make picture)
add a private instance variable of type double called replacementCost, which is (you ready??) the cost to replace this item when it's used up
add a private instance variable of type int called usesLeft, which is the number of times the ConsumablePart can be used before it must be replaced.
Override fail() in both ExpendablePart and ConsumablePart

In ExpendablePart.fail(), the message (in addition to identifying the part) should include that the failure was an expendable part, and that it will take leadTime days to replace the part
In ConsumablePart.fail(), the message (in addition to identifying the part) should include that the failure was a consumable part, and that it will cost replacementCost dollars to replace the part.
 
