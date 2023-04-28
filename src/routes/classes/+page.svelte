<script>
    import {
        Heading,
        P,
        A,
        Mark,
        Secondary,
        Table,
        TableBody,
        TableBodyCell,
        TableBodyRow,
        TableHead,
        TableHeadCell,
        Checkbox,
        TableSearch,
        Kbd
    } from "flowbite-svelte";
</script>

<div class="pt-20 m-10 mx-36">
    <Heading tag="h2" class="mb-4">Writing Classes</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Anatomy of a Class</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        A class in Java is made up of attributes (also called instance variables), methods, 
        and constructors. Attributes are declared using the private keyword, which restricts 
        access to only the declaring class. Constructors are used to set the initial state of 
        an object's attributes. Methods can be both public and private, and are used to operate 
        on an object's attributes. Data encapsulation and implementation of a class are hidden 
        from outside the class. Accessor and mutator methods allow the use and modification of data.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Constructors</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Constructors are used to set the initial state of an object's attributes. Constructor 
        parameters are local variables to the constructor and set instance variables. If no 
        constructor is written, Java provides a no-argument constructor, and instance variables 
        are set to default values.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Documentation</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Comments in Java can be single-line (// ), multiline (/* */), or Javadoc (/** */). 
        Javadoc comments are used to create API documentation. Use comments to describe 
        functionality and document preconditions and postconditions. Precondition 
        comments describe conditions that must be true before a segment of the program 
        can be executed. Postcondition comments describe conditions that are true after a 
        segment of the program has executed. Programmers write method code to satisfy 
        postconditions when preconditions are met.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Accessor and Mutator Methods</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Accessor methods are used to get the value of instance or static variables. Mutator 
        methods are used to set the value of instance or static variables. Accessor methods 
        are non-void and return a copy of the value. Mutator methods are often void methods 
        with parameters.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Writing Methods</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Methods can define the behaviors of an object. It is possible to pass objects into 
        methods. Do not modify mutable objects that are passed in, as this will change the 
        original object. When the parameter is a primitive, the formal parameter copies the 
        value. When the parameter is a reference to an object, the formal parameter copies 
        the reference. Passing in a reference results in the formal parameter and the actual 
        parameter referring to the same object.<br>
        An example of a method that passes in a object is:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public boolean isSameBreed (Dog otherDog) &lbrace;<br>
        ⠀⠀return breed.equals(otherDog.breed);<br>
        &rbrace;<br>
        //breed is private data in the dog class<br>
        //method is in the dog class, object passed in is also part of dog class<br>
        //allows both calling object and parameter to access breed
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Static Variables and Methods</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Static means associated with the class, not the object. Static methods include a 
        static header before the method name. Static methods cannot access instance variables 
        but can access and change static variables. They do not have a "this" reference. 
        All objects of a class share a single static variable, which can be either public 
        or private and is designated with the static keyword before the variable type.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Scope and Access</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Local variables are declared within the body of a method or constructor and can 
        only be used within that method or constructor. Local variables cannot be declared 
        public or private. If a local variable has the same name as an instance variable, 
        the variable name will refer to the local variable instead of the instance variable. 
        Programmers can solve large problems by splitting them into subproblems and creating 
        methods to solve each subproblem.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">The "this" Keyword</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Within a non-static method or constructor, "this" refers to the current object. 
        "this" can be used to pass the current object as a parameter in a method call.
    </P>
</div>