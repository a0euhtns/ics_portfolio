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
    <Heading tag="h2" class="mb-4">Inheritance</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Inheritance Relations</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Inheritance in Java involves a parent-child relationship between classes. The common 
        attributes of related classes can be put into a superclass, which is the parent class. 
        The classes that extend a superclass are called subclasses, and they inherit the 
        attributes and behaviors of the parent class. This is called an is-a relationship, 
        and it can be represented as a directed graph from the parent pointing to the child. 
        The <Kbd class="px-1.5 py-1 font-mono font-semibold">extends</Kbd> keyword means that 
        a class inherits from another class, and a class can only extend one other class.
    </P>

    <Heading tag="h4" weight="light" class="mb-4">The Super Keyword</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        When a subclass is created, the constructors are not inherited through inheritance. 
        The <Kbd class="px-1.5 py-1 font-mono font-semibold">super</Kbd> keyword is used to 
        call anything from the parent, but only the first line of the subclass constructor can 
        call <Kbd class="px-1.5 py-1 font-mono font-semibold">super</Kbd>. Parameters can be 
        passed in <Kbd class="px-1.5 py-1 font-mono font-semibold">super</Kbd>, which calls 
        whichever constructor with a matching signature. If a subclass constructor does not 
        call <Kbd class="px-1.5 py-1 font-mono font-semibold">super</Kbd>, Java inserts a call 
        to the superclass's no-argument constructor. Regardless of whether the superclass constructor 
        is called implicitly or explicitly, the superclass constructors call each other until the 
        Java Object constructor is called, and then it goes back down the hierarchy.
        <br><br>

        The <Kbd class="px-1.5 py-1 font-mono font-semibold">super</Kbd> keyword can also be used to call methods. 
        The syntax <Kbd class="px-1.5 py-1 font-mono font-semibold">super.method()</Kbd> is used to 
        call a valid method name and parameters. <Kbd class="px-1.5 py-1 font-mono font-semibold">super</Kbd> 
        can call overridden methods in a subclass, almost like a recursion call stack.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Method Overriding</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Method overriding is when a public method in a subclass has the same signature as a public method in the 
        superclass. Subclasses inherit all public methods, which remain public in the subclass. When 
        calling an overridden method, Java calls the method of the original object.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Reference Variables</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        If class S "is-a" class T, assigning an object of type S to a reference of type T allows 
        polymorphism. Polymorphic means that you can refer to objects from different classes, and 
        when calling an overridden method, Java calls the method of the original object. If S "is-a" T, 
        a reference of T can be used for T or S. This can be useful to store every class in one data 
        structure.
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public class T &lbrace;<br>
        ⠀⠀public act() &lbrace;<br>
        ⠀⠀⠀⠀// implementation not shown<br>
        ⠀⠀&rbrace;<br>
        &rbrace;<br><br>

        public class S extends T &lbrace;<br>
        ⠀⠀public act() &lbrace;<br>
        ⠀⠀⠀⠀// different implementation<br>
        ⠀⠀&rbrace;<br>
        &rbrace;<br><br>

        // another class<br>
        T obj = new S(); // obj has a reference variable of type T
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Polymorphism</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        At compile time, methods in or inherited by the declared type determine the correctness 
        of a non-static method call. The correct method based on the actual object type is run, 
        not the reference variable. When an object's reference type is parent, it can be 
        downcasted to the original object type using the syntax 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">((Subclass)class).method();</Kbd>. 
        Brackets must be used as the method operator take precedence over casting. Polymorphism 
        only applies when a method is overridden; a method that doesn't exist in the parent 
        would give an error if the reference type is parent.
        <br><br>

        In the example,
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        // another class
        T obj = new S(); // obj has a reference variable of type T
        obj.act(); // class S
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        If obj.act() is called, Java would find the act method that fits the object's actual type, 
        not the reference variable type. obj.act() would execute the method from class S.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Downcasting</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        When an object's reference variable is a parent, it can be cast to anything below the 
        parent class to the object's class. This is used to access methods of different classes.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Abstract Classes</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Abstract classes are superclasses that are only a concept and cannot be instantiated. 
        Abstract classes have no implementation of code, and if a class has one or more abstract methods, 
        it must be declared abstract. Abstract classes can still have constructors. If a 
        subclass of an abstract class does not have implementation of all abstract methods, 
        it must also be declared abstract.
        <br><br>

        An abstract class is declared with:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        abstract class Class &lbrace;&rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        An abstact method can be declared as:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public abstract void method();
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Interfaces</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Interfaces are like abstract classes, but they do not have fields or constructors, 
        and all methods are abstract. If a class uses an interface, it can be declared 
        using the syntax:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        interface Interface &lbrace;&rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        A class can implement an interface with:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        class Class implements Interface &lbrace;&rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        A class can implement multiple interfaces but only extend one superclass. Finally, 
        an interface can still be used as a reference variable for an object, as long as 
        the object implements the interface. This is useful as it can help apply polymorphism.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Object Class</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        The object class is the superclass of all objects, all classes automatically extend 
        the object class, even when not specified. The object class has the 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">equals(Object other)</Kbd> method, 
        which can check if 2 objects are equal and returns a boolean. It also has the 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">toString()</Kbd> method, which can be 
        used to print an object. These methods are often overwritten to provide more functionality. 
        The <Kbd class="px-1.5 py-1 font-mono font-semibold">instanceof</Kbd> operator can be used 
        to check if an object is an instance of a specified class. Finally, all objects can have 
        the object class reference variable associated with it.
    </P>
</div>