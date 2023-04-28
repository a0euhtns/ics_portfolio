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
        P
    } from "flowbite-svelte";
</script>
<div class="pt-20">
    {@html `<pre><code>
Using Objects
Instances of Classes


class is blueprint for creating objects with defined behaviors and attributes
object is a specific entity made from a class
objects are instances with classes, variable names
objects have behaviors and attributes defined by the class
If 2 variables refer to the same object, each change will affect both.
Creating Objects


constructors are used to initialize attributes

 public Person(String nm, int ag, boolean ad) { //formal parameters
		name = nm;
		age = ag;
		isAdult = ad;
}

Person bob = new Person("bob", 15, false); //actual parameters


constructors can be overloaded, multiple constructors with different parameters


default constructor, no parameters
if an object is declared but not initialized, it is null


null, special value to indicate that it is not associated with any object
Calling Void Methods


calling methods, method();
if you are calling a method of an object, objectName.method();
not class name
NullPointerException if object is not initialized
with parameters, method(a, b);
types must match
methods can be overloaded, different parameter lists
for similar tasks
Calling Non-Void Method


returns a value based on method signature
return value must be stored in a variable or used in an expression
String Objects and Methods


string objects may be initialized with:


double quotes
new String(””);
Strings are immutable, cannot be changed


concatenation


joins strings together
+= joins and redefines variable
primitives can be concatenated, converted to string
escape sequences


\”, \\, \n
double quote, backslash, new line
string methods


csajqr string method document
substring(a, b) does not include index b



Wrapper Classes


wrapper classes convert primitives to reference types
autoboxing
automatic conversion from primitive to wrapper
passed as a parameter to a method that expects wrapper
assigned to variable of the wrapper class
unboxing
automatic conversion from wrapper to primitive
passed as a parameter to a method that expects primitive
assigned to variable of primitive type
Math Class


static methods
call the class name Math
part of the java.lang package
check jqr
Math.random()
random double 0.0 ≤ x < 1.0
random number from 25 to 60 is
(int)(Math.random()*36)+25

    </code></pre>`}
</div>