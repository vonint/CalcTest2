Note: This repository is now set to "read-only" and development of the application is halted.
"CalcTest2" was a very simple console-based application written in C++. Its purpose was for me to attempt to apply some of what I was learning from the page [LearnCpp](https://www.learncpp.com/) in the form of a simple calculator.
This application has served its intended purpose and is no longer under development.

I have now attached the UNLICENSE "license" to this repository, thus hereby releasing it to the public domain (as-is).

Date: July 16th, 2023

<details>
  <summary>CalcTest2: Application README</summary>
 
  # CalcTest2

### This console-only application contains basic arithmetic functions as a proof-of-learning milestone for myself and is not intended for production. Release included for testing.
[Click here to check out my old CalcTest1 application (which is no longer maintained).](https://github.com/von-de/CalcTest1)

# Version 1.2 - Fixes & UX/UI improvements

Changelog:
- Overhauled the systems functions use to call each other
- One function no logner depends on another call to return to caller
- Function userInputControl is now split into userInputOverview and userInput to allow for more design freedom
- Function userInputOverview now returns to void
- Added additional batch arguments to start of main (echo off, console title, console color)
- Adjustment to calculation UI, result screen now makes clear that the result does not get saved
- Typing in an invalid value into userInput now causes an error to be displayed above userInputOverview without confirmation prompt

#### Desired changes: 
- Display an error instead of "1" if calculation results in a non-int
- Prevent issues caused by the divisor "0" (dividing through zero)

<sub>Date of finish: 26.10.2022, 14:41 CEST</sub>

## Version 1.1.1 - Hotfix

Changelog:
- Functions userInputControl, userIf and userTextGen now return 0 to caller in all if-statements and at the end of execution, instead of calling another function and returning by calling the caller function. This temporary fix prevents potential errors or faults if the program returns to the caller in an unexpected way.
- In a future update, a better solution will be integrated.

<sub>Date of finish: 26.10.2022, 13:51 CEST</sub>

# Version 1.1 - Application improvements

Changelog:
- Function refactor to allow improvements
- Implemented loop to "menu" (aka userInputControl) through function calls depending on the integer passed
- On subsequent returns to menu, do not show userFirstOpen message
- Exit message should now only display when entering "5" in menu to exit the program
- Changes to header file to reflect changes
- Added and commented out preprocessor directive as a reminder to include README in the future
- README now uses hyphens instead of asterisks for lists
- README and future release tags now use subscript for dates instead of regular text (retroactively applied on README)
- Updated bad descriptions in Version 1.0 release notes

#### Desired changes: 
- Switch to C++ solution for pause and clear (currently uses batch arguments passed to console)

<sub>Date of finish: 26.10.2022, 09:37 CEST</sub>

# Version 1.0 - Initial release

Features:
* Forward declarations through a guarded header
* Separate functions dedicated to each program segment:

   * Main function
   * "First Open" function (introduction message on first open)
   * Input function (returns user input to main)
   * If function (takes input from main and calls one of the following functions depending on given input; returns 0 on invalid input)
   * Addition function (returns to if)
   * Subtraction function (returns to if)
   * Multiplication function (returns to if)
   * Division function (returns to if)
   * Exit function (called after if returns to main and shows a message and waits for user confirmation to exit the program)

* Simple 5 choices prompt with user input (through "cin")
* Basic addition (first and second summand)
* Basic subtraction (minuend and subtrahend)
* Basic multiplication (first and second factor)
* Basic division (dividend and divisor)
(To be improved: Invalid entries return prematurely to main and subsequently cause a program exit)
* Currently uses batch arguments passed to console

<sub>Date of finish: 25.10.2022, 23:51 CEST</sub>
</details>
