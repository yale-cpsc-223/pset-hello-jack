# Pset 0: "Hello, Jack!"

## Due Date: 2023-01-27 11:59 PM NHT (New Haven Time)

## Purpose
This assignment is designed to familiarize you with a C development environment and the Gradescope submission system.
It is *not* designed to be an intellectual challenge nor to be tedious.

## Assignment
Write a C program that greets the user with their name.
It must do the following:
* Check the command-line arguments. If there is more than one (1) argument, the second argument is interpreted as the user's name
* If there is exactly one command-line argument, the program should prompt the user to enter their name by displaying the string, `"What is your name? "`. Thereafter the program must read input from `stdin` until a newline character and treat that input as the user's name (excluding the newline character).
* Once the program has the user's name, it must print the string `"Hello, "` followed by the user's name and a newline character.

## Example Interaction
Here is a sample interaction (lines beginning with `$` are command prompts):
```
$ ./Hello
What is your name? Alan
Hello, Alan
$
```

Here is a sample interaction in which the name is provided as a command-line argument (lines beginning with `$` are command prompts):
```
$ ./Hello Ozan
Hello, Ozan
$
```

## Assumptions About the Input
In each assignment, there will be some assumptions you are permitted to make about the nature of the input.
**Your submission will not be tested with input that violates these assumptions and you will not be graded on your program's behavior with input that violates these assumptions.**

For this assignment, there are some assumptions you may make about the composition of the user's name.
1. The user's name will not contain any newline characters within it
2. The user's name will not be longer than 128 characters

## Submission
Submit this assignment to Gradescope by uploading a `.zip` archive containing (at least) the following files:
* All C source and header files needed to compile and run your program
* A `makefile` with a target called `Hello` that creates an executable named `Hello` which, when run, satisfies the requirements above. This file may be named either `makefile` or `Makefile`
* `LOG.md`, which is a text file. It must conform to the format specified in section [Log File](#log-file)

## Log file

Your `LOG.md` file should be a [markdown](https://www.markdownguide.org/) file of the general form (that below is mostly fictitious):

```markdown
# Author
Alan Weide 
adw58

# Estimate of time to complete assignment
10 hours

# Actual time to complete assignment
| Date | Time Started | Time Spent | Work completed |
| :--: | -----------: | ---------: | :------------- |
| 8/01 |      10:15pm |       0:45 | read assignment and played several games to help me understand the rules. |
| 8/02 |       9:00am |       2:20 | wrote functions for determining whether a roll is three of a kind, four of a kind, and all the other lower categories |
| 8/04 |       4:45pm |       1:15 | wrote code to create the graph for the components |
| 8/05 |       7:05pm |       2:00 | discovered and corrected two logical errors; code now passes all tests except where choice is Yahtzee |
| 8/07 |      11:00am |       1:35 | finished debugging; program passes all public tests |
|      |              |            |                |
|      |              |       7:55 | total time spent |

# Collaboration
I discussed my solution with: Petey Salovey, Biddy Martin, and Biff Linnane
(and watched four episodes of Futurama).

# Discussion
Debugging the graph construction was difficult because the size of the
graph made it impossible to check by hand.  Using asserts helped
tremendously, as did counting the incoming and outgoing edges for
each vertex.  The other major problem was my use of two different variables
in the same function called _score and score.  The last bug ended up being
using one in place of the other; I now realize the danger of having two
variables with names varying only in punctuation -- since they both sound
the same when reading the code back in my head it was not obvious when
I was using the wrong one.
```

Specifically, it must contain...
* Your full name and netID, each on their own line in a section with header "`# Author`"
* Your estimate of the time required (made prior to writing any code) in a section with header "`# Estimate of time to complete assignment`"

* The total time you actually spent on the assignment, formatted as you see fit[^1], but must contain each "shift" during which you worked on the assignment and a brief description of the work completed in each shift, in a section with header "`# Actual time to complete assignment`"

* The names of all others (but not members of the teaching staff) with whom you discussed the assignment for more than 10 minutes, in a section with header "`# Collaboration`", and

* A brief discussion (~100 words) of the major conceptual and coding difficulties that you encountered in developing and debugging the program (and there will always be some), in a section with header "`# Discussion`", which must be the last section

[^1]: In the example, it is formatted as a table.
