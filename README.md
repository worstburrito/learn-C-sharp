# Learn C# in ONE Day

## Table of Contents
1. [Comments](#comments)
2. [Variables and Operators](#variables-and-operators)
3. [Arrays, Strings, Lists](#arrays-strings-lists)
4. [Making Programs Interactive](#making-programs-interactive)



---

## Comments

```c#
// This is a comment
// This is another comment
// This is yet another comment

/* This is a comment
This is another comment
This is yet another comment
*/
```

## Variables and Operators
```c#
/* int - integer i.e. numbers with no decimal or fractional parts
byte - integral numbers, ranges from 0 to 255
float - floating point numbers i.e. numbers with decimal places. Rounds off after 7 digits.
double - also a floating point number but can store a much wider range of numbers.
decimal - smaller range than float or double.
char - is a single Unicode characater
bool - true or false */

// Initializing a Variable
byte userAge = 20;
int numberOfEmployees = 510;
char grade = 'A';
bool promote = true;

// Delcaring, then Initializing
byte year;
year = 20;

// Basic Operators: +, -, *, /, %

// More Assignment Operators

x = x + 2; // This could be written instead:
x += 2;

x = x + 1; // This is equivalent to:
x++;

// Type Casting

int x = (int) 20.9; // Type casting 20.9 into an int results in 20.9 turning into 20.
```

## Arrays, Strings, Lists

### Arrays
```c#
// Array: collection of related data
int[] userAge = {21, 22, 23, 24, 25};

// Declare then Initialize:
int[] userAge2
userAge2 = new [] {21, 22, 23, 24, 25};

// Declaure and initialize with default values:
int[] userAge3 = new int[5];
// This becomes {0, 0, 0, 0, 0}

// Update individual values
userAge[0] = 31;
// The array now becomes: {31, 22, 23, 24, 25}

// If you type:
userAge[2] = userAge[2] + 20;
// The array now becomes: {31, 22, 43, 24, 25}

// Array Properties and Methods

// Length
int [] userAge = {21, 22, 26, 32, 40};
userAge.Length // is equal to 5 for the 5 numbers in the array

// Copy()
int [] source = {12, 1, 5, -2, 16, 14};
int [] dest = {1, 2, 3, 4};
Array.Copy(source, dest, 3); // dest now becomes {12, 1, 5, 4}

// Sort()
int [] numbers = {12, 1, 5, -2, 16, 14};
Array.Sort(numbers);
// numbers now becomes {-2, 1, 5, 12, 14, 16}

// IndexOf()
int [] numbers = {10, 30, 44, 21, 51, 21, 61, 24, 14};
int ans = Array.IndexOf(numbers, 21); // ans = 3 because that's where 21 is

ans = Array.IndexOf(numbers, 100); // ans = -1 because 100 doesn't exist
```

### Strings
```c#
// Strings: a piece of text, "Hello World"
string message = "Hello World";

// Assign empty string to a variable
string anotherMessage = "";

// Concatenating Strings
string myName = "Hello World, " + "my name is Jamie";

// String Properties and Methods

// Length
"Hello World".Length // this equals 11, and counts the space

//Substring()
string message = "Hello World";
string newMessage = message.Substring(2, 5); // this equals "llo W"

// Equals()
string firstString = "This is Jamie";
string secondString = "Hello";

firstString.Equals("This is James"); // returns true
firstString.Equals(secondString); // returns false

// Split()
/* Requires two arguments - an array os strings to act as separators
and a second argument to specific whether you want to remove empty
strings from the result. */

string [] seperator = {", ", "; "};
string names = "Peter, John; Andy, , David";
string [] substrings = names.Split(seperator, StringSplitOptions.None);

/* Line 1: first declare an array of two strings to act as seperators
Line 2: assign the string we want to split
Line 3: we use the names var to call the Split() method
The result: {"Peter", "John", "Andy", "", "David"} */
```
### Lists
```c#
// Lists: Similar to Arrays, but elements can be added or removed at will.
List<int> userAgeList = new List<int>();
List<int> userAgeList = new List<int> {11, 21, 31, 41};

// To access elements,  use the same notation as array
userAgeList[2] // 2 is the index of the element, which is 31.

// List Properties and Methods

// Add()
userAgeList.Add(51);
userAgeList.Add(61);
// userAgeList now has 6 numbers {11, 21, 31, 41, 51, 61}

// Count
userAgeList.Count; // = 6 numbers

// Insert()
userAgeList.Insert(2, 51);
//userAgeList now becomes {11, 21, 51, 31, 41, 51, 61}

// Remove()
userAgeList.Remove(51); // removes the first instance of 51
// userAgeList now becomes {11, 21, 31, 41, 51, 61}

// RemoveAt()
userAgeList.RemoveAt(3); // this removes the 4th element at index 3
// userAgeList now becomes {11, 21, 31, 51, 61}

// Contains()
userAgeList.Contains(51); // results as true

// Clear()
userAgeList.Clear(); // removes all elements from list

```

## Making Programs Interactive
```c#
// To display messages to our users, use Write() or WriteLine()

Console.WriteLine("Hello ");
Console.WriteLine("How are you?");
/* We get:
Hello
How are you?*/

Console.Write("Hello ");
Console.Write("How are you?");
/* We get:
Hello How are you?*/

// Example 1: Strings
Console.WriteLine("Hello, how are you?");
// Output = Hello, how are you?

// Example 2: Int
int userAge = 30;
Console.WriteLine(userAge);
// Output = 30

// Example 3: Concatenate
Console.WriteLine("Hello, " + "how are you?" + " I love C#.");
// Output = Hello, how are you? I love C#.

// Example 4: Concatenate Strings and Variables
int results = 79;
Console.WriteLine("You scored " + results + " points on your test!");
// Output = You scored 79 points on your test!

```


## Title
```c#

```
