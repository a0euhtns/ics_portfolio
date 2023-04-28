<script>
    import {
        Navbar,
        NavBrand,
        NavLi,
        NavUl,
        NavHamburger,
        Dropdown,
        DropdownItem,
        Chevron,
    } from "flowbite-svelte";
</script>
<div class="pt-20">
    {@html `<pre><code>
Writing Classes
Anatomy of a Class
public and private affect access
private restricts access to only declaring class
classes are designated public
attributes are private
constructors are public
methods can be both
cannot access private methods outside of class
data encapsulation, implementation of a class are hidden
instance variables encapsulated using private
accessor and mutator methods allows use and modification of data
Constructors
object state refers to its attributes
has-a relationship
constructors set initial state of object for all instance variables
constructor parameters are local variables to the constructor, sets instance variables
no constructor written, java provides no-argument constructor, instance variables set to default values
null can be set
Documentation
comments are ignored


single (//), multiline (/* /), javadoc (/** */)


javadoc comments help create API documentation


use comments to describe functionality


precondition - always true prior to execution of a segment of the program


comment conditions that are true for method to work
postcondition - always true after execution of a segment of a program


comment conditions that are true after method is run
precondition - postcondition

 /**
  * Precondition: Parameter num is less than the length of the word
  * Postcondition: Returns the string from index num to end of the word
  *                followed by the characters of word from index 0 to num
  *                not including num. The state of word is not changed


programmers write method code to satisfy postconditions when preconditions are met


Accessor Methods
gets value of instance or static variables
non-void
copy of the value is returned, return by value
toString usually overridden to provide a description of a specific object
includes data from instance variables
if you print an object that has a toString method, it calls the method and prints the returned string
Mutator Methods
sets value of instance or static variables
often void method with parameters
Writing Methods
you can pass objects into methods


dog example

 public boolean isSameBreed (Dog otherDog) {
	return breed.equals(otherDog.breed);
}
//breed is private data in the dog class
//method is in the dog class, object passed in is also part of dog class
//allows both calling object and parameter to access breed


methods can define the behaviors of an object


don't modify mutable objects that are passed in


change original
when parameter is a primitive, formal parameter copies the value


when parameter is a reference to an object, formal parameter copies the reference


passing in reference results in formal parameter and actual parameter to refer to the same object


Static Variables and Methods
static means associated with class, not object
static methods include static header before method name
cannot access instance variables
can access and change static variables
do not have a “this” reference
all objects of a class share a single static variable
can be either public or private, designated with static before variable type
used with class name and dot operator, since they are part of the class, not object
Scope and Access
local variables - declared within the body of a method or constructor
cannot be declared public and private
local variable with same name as an instance, variable name will refer to local instead of instance
local variables in a method or constructor can only be used within
programmers can solve large problems by splitting into subproblems and creating methods to solve each subproblem
method decomposition
this Keyword
within a non-static method or constructor
“this” refers to current object
“this” can be used to pass the current object as a parameter in a method call

    </code></pre>`}
</div>