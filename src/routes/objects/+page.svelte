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
    <Heading tag="h2" class="mb-4">Using Objects</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Instances of Classes</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        A class is a blueprint for creating objects with defined behaviors and attributes. 
        An object is a specific entity made from a class. Objects are instances with classes and 
        variable names. Objects have behaviors and attributes defined by the class. If two 
        variables refer to the same object, each change will affect both.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Creating Objects</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Constructors are used to initialize attributes. They have the same name as the class 
        and are defined without a return type. The code below is an example of a constructor 
        for a <Kbd class="px-1.5 py-1 font-mono font-semibold">Person</Kbd> class:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public Person(String nm, int ag, boolean ad) &lbrace; // formal parameters<br>
        ⠀⠀name = nm;<br>
        ⠀⠀age = ag;<br>
        ⠀⠀isAdult = ad;<br>
        &rbrace;<br>
        <br>
        // in a separate class<br>
        Person bob = new Person("bob", 15, false); // actual parameters  
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Constructors can be overloaded, meaning there can be multiple constructors with different 
        parameters, including a default constructor with no parameters. If an object is declared 
        but not initialized, it is null, a special value that indicates it is not associated with 
        any object.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Calling Void Methods</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Methods are called by their name followed by parentheses. If you are calling a method of 
        an object, use <Kbd class="px-1.5 py-1 font-mono font-semibold">objectName.method()</Kbd>, 
        not the class name. A <Kbd class="px-1.5 py-1 font-mono font-semibold">NullPointerException</Kbd> 
        will be thrown if the object is not initialized. Methods with parameters require the types to 
        match. Methods can also be overloaded, meaning they can have different parameter lists 
        for similar tasks.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Calling Non-Void Methods</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        A non-void method returns a value based on the method signature. The return value must be stored 
        in a variable or used in an expression.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">String Objects and Methods</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        String objects may be initialized with double quotes or <Kbd class="px-1.5 py-1 font-mono font-semibold">new String("value")</Kbd>. 
        Strings are immutable and cannot be changed. Concatenation joins strings together, 
        and <Kbd class="px-1.5 py-1 font-mono font-semibold">+=</Kbd> joins and redefines a variable. 
        Primitives can be concatenated and converted to a string. Escape sequences such as <Kbd class="px-1.5 py-1 font-mono font-semibold">\"</Kbd>, 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">\\</Kbd>, and <Kbd class="px-1.5 py-1 font-mono font-semibold">\n</Kbd> 
        represent a double quote, a backslash, and a new line, respectively. String methods are listed in the APCSA JQR document. 
        One example of a string method is the <Kbd class="px-1.5 py-1 font-mono font-semibold">substring(a, b)</Kbd> method, 
        which returns a String from index a to index b, but not including it.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Wrapper Classes</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Wrapper classes convert primitives to reference types. Autoboxing is the automatic conversion 
        from primitive to wrapper. It can be passed as a parameter to a method that expects a wrapper 
        or assigned to a variable of the wrapper class. Unboxing is the automatic conversion from a 
        wrapper to a primitive. It can be passed as a parameter to a method that expects a primitive 
        or assigned to a variable of primitive type.<br><br>
        Here's an example of using a wrapper class to convert a primitive to a reference type and perform autoboxing:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int num = 42; // primitive int<br>
        Integer numObj = num; // autoboxing - converting primitive to Integer object<br>
        System.out.println(numObj); // prints "42"
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        And here's an example of using a wrapper class to convert a reference type back to a primitive and perform unboxing:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        Double doubleObj = 3.14; // Double object
        double num = doubleObj; // unboxing - converting Double object to primitive double
        System.out.println(num); // prints "3.14"  
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Math Class</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        The Math class provides static methods that are called using the class name Math. 
        It is part of the java.lang package. The Math.random() method generates a random 
        double from 0 (inclusive) to 1 (exclusive). An example of generating a random number 
        from 25 to 60 is:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int rand = (int)(Math.random()*36)+25 // random number from 0 - 35, 25 is added.
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        The full list of Math class methods can be found in the JQR.
    </P>
</div>
