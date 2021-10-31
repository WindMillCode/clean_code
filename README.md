# Left of pg 52

# Meaningful Namess

* dont use single letters, makes it hard to search for
* dont encode variable names
* the class should be small enough where you dont have to prefix
* dont be cute
    * say what you mean ,mean what you say
* pick one word per concept
    * not fetch,retrieve,get, just get 
* dont use same word for 2 different concepts
* choose technicalNames, programmers know what you mean
* if it needed a comment an issue
* use prefixes for context or context object 
    * not too much context
```ts
// good
couchAccount

// bad
couchFromMacysAndPjAccount

```
# Functions
* keep functions small
* functions do one thing
    * section with in functions, cant reasonably do one thing
* theres level of abstractation
    * lowe level -  .append("/n")
    * medium level - String pagePathName = PathParser.render(pagePath);
    * high level - getHtml();
* longer descriptive name is better
* a fn should have no argunments, greatest is 2 
* flag args are bad
    * violates SRP, if true do x, else do y
* make argument objects
* make arg lists
* use keywords to remember the order of args
    instead of equals use, expectedEqualActual(expected,actual)
* side effect, a function does not do what its supposed to
* functions should either change the state of an object or return information
* sepearte try catch from acutal function
    * functions that handle errors should only do that

# Comments
* a necessary evil
* cant realisitically maintain  comments
* comments dont make up for bad code*
* if you have to explain yourself use a function
* we need legal comments 
* good for explaing regexp
* good for intent
* good for warnings
    * ex: // dont run DAST unless you have time to kill
* banners of demarcation are ususally ignored
* avoid commented out code?
* tmi


# Formatting
* put spaces between thoughts in your code
* avoid protected vairables
* instance variables are used in many methods of the class
    * everyone should know where instance variables are
* if one fn calls another they should be vertically close
* there is conceptual affinitiy
* programmers prefer short lines
* 120 max limit for programming
* aligned decorratores make your eyes forget the actual important  details
* rmbr indentation always make code that can scale


# Variables 
* keep them public
* dont expose details of data keep in abstract terms

```java
public interface Vehicle {
 double getFuelTankCapacityInGallons();
double getGallonsOfGasoline();a
}
```

* this is preferabble
```java
public interface Vehicle {
 double getPercentFuelRemaining();
}
```
* __law of demeter__
* method f of class C should only call methods of
    * C
    * object created by f
    * object passed as an arg to f
    *  An object held in an instance variable of C
    * not invoke methods on object that are returned
* if we have an object we should be telling it to do something not asking about it's intnernals



## Questions 
* not understanding the law of demeter too well, to clarify i should use properties on the object to get what I need I should use a methods that does it for me
    * according to demeters law - Objects expose behavior and hide data, Data structures expose data and have no significant behavior

# Objects and Data Stuctures
