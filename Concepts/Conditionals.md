While you could theoretically write your entire program sequentially, detailing how to handle every possible outcome step by step, this would likely take you forever and well does not really consider the possibility of making decisions...what if the user doesn't want to add a hat to their character in your text based game?

> "In the mall swiping cards Decisions, Decisions"

That's where we utilise conditions. These exist in all programming languages and for the most part work the same. The two main conditions we'll really be taking a look at are [[#If Statement]], and the [[#Case Statement]] (often referred to as Switch Statement).

The general principal of conditions comes to a simple yes or no question. If our defined and or logical condition is met successfully (true), the computer will execute the appropriate set of instructions, and act appropriately when false. 

## If Statement

![[condition.png]]
The if statement is basically the core of most computing. EVERYTHING IS AN IF STATEMENT. I say that as a joke, but in reality everything your machine does based of a condition being met, from inputting a character on the screen to playing a sound on the speakers.

These can be very basic...

```vb
IF (condition) THEN
	'Execute Code'
	ELSE
	'Execute alternative'
END IF
```

But you can also begin nesting them- and it grows very quickly- For example the if-else-if:

```vb
IF (condition1) THEN
	'Execute Code'
	ELSE IF (condition2) THEN
		'Other possibility'
	END IF
	ELSE
		'Execute alternative'
END IF
```

It gets crazier and can get really bad. I would personally advise against using too many of these statements as it can get very ugly, very fast...

![[yandare-if.png]]

This mess can be fixed with the next conditional...

## Case Statement
