# Truffula Notes
As part of Wave 0, please fill out notes for each of the below files. They are in the order I recommend you go through them. A few bullet points for each file is enough. You don't need to have a perfect understanding of everything, but you should work to gain an idea of how the project is structured and what you'll need to implement. Note that there are programming techniques used here that we have not covered in class! You will need to do some light research around things like enums and and `java.io.File`.

PLEASE MAKE FREQUENT COMMITS AS YOU FILL OUT THIS FILE.

## App.java

The application interface, based on the users input command prints a directory tree with colors, hidden files shown, or custom root directories.

## ConsoleColor.java

The central area for providing color names and their assigned ANSI codes under an enum. Functions such as getCode() provide the ANSI escape code associated with the color. Also contains a ConsoleColor constructor.

## ColorPrinter.java / ColorPrinterTest.java

The ColorPrinter class acts as a vector to access special printing privelages, in this case printing with colors internally set based on the enumerator definition. For this enumerator, ConsoleColor.RED is an example of these options, swapping out the final color should change the color of the message accordingly.

The Test asks whether the color is automatically set to ConsoleColor.RESET outside the variable after the area where the print is finished.

## TruffulaOptions.java / TruffulaOptionsTest.java

Forms a directory tree based on settings defined in its call by App.java. Acts as the error handler and coordinator for passed in argument handling. Utilized previous two files as the backbone of its color display and printing.

TruffulaOptionsTest.java checks if the directory is set correctly, all in the name of the test. Future tests should check if blank or improper arguments have been handled correctly.

## TruffulaPrinter.java / TruffulaPrinterTest.java

How the tree is printed, the color order when printing, the output printer for displaying said data, and example display structure are all handled in TruffulaPrinter.java.

The Test simply checks if a valid directory has been set.

## AlphabeticalFileSorter.java

Just sorts by alphabet in the sort() section. (File sorting.)