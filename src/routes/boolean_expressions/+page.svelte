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
    <Heading tag="h2" class="mb-4">Boolean Expressions</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Relational Operators</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Relational operators are used to compare two values and return a Boolean value. 
        The six relational operators in Java are:
        <ul class="list-disc pl-8">
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">==</Kbd> equal to</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">!=</Kbd> not equal to</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">&gt;</Kbd> greater than</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">&lt;</Kbd> less than</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">&gt;=</Kbd> greater than or equal to</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">&lt;=</Kbd> less than or equal to</li>
        </ul>
        For example, to check if two numbers are equal:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int num1 = 5;<br>
        int num2 = 7; <br>
        if (num1 == num2) &lbrace;<br>
        ⠀⠀System.out.println("The numbers are equal.");<br>
        &rbrace; else &lbrace;<br>
        ⠀⠀System.out.println("The numbers are not equal."); // prints this<br>
        &rbrace;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Logical Operators</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Logical operators are used to combine Boolean expressions and return a Boolean value. 
        The three logical operators in Java are:
        <ul class="list-disc pl-8">
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">&&</Kbd> logical AND</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">||</Kbd> logical OR</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">!</Kbd> logical NOT</li>
        </ul>
        For example, to check if a number is between 1 and 10:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int num = 5;<br>
        if (num &gt;= 1 && num &lt;= 10) &lbrace;<br>
        ⠀⠀System.out.println(num + " is between 1 and 10."); // prints this<br>
        &rbrace; else &lbrace;<br>
        ⠀⠀System.out.println(num + " is not between 1 and 10.");<br>
        &rbrace;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Boolean Variables</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Boolean variables are variables that can only have the value true or false. They are 
        often used to store the result of a Boolean expression. The basic syntax for declaring 
        a Boolean variable is
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        boolean varName;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        For example, to declare a Boolean variable and assign it the value of a Boolean expression:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int num1 = 5;<br>
        int num2 = 7;<br>
        boolean isEqual = num1 == num2; // isEqual = false<br>
        System.out.println("The numbers are equal: " + isEqual);
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Short-Circuit Evaluation</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Short-circuit evaluation is a feature of logical operators in Java that can improve program 
        performance. When evaluating a logical expression using the 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">&&</Kbd> or 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">||</Kbd> operators, Java only 
        evaluates the second operand if necessary.
        <br>
        For example, if the first operand of a logical AND expression is false, then the entire 
        expression is false regardless of the value of the second operand. In this case, Java does 
        not evaluate the second operand. Similarly, if the first operand of a logical OR expression 
        is true, then the entire expression is true regardless of the value of the second operand.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">If, Else-if and Else Statements</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        If/else if/else statements are used to execute different code blocks based on 
        different conditions. The syntax for an if/else if/else statement is as follows:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        if (condition1) &lbrace;<br>
        ⠀⠀// code block 1<br>
        &rbrace; else if (condition2) &lbrace;<br>
        ⠀⠀// code block 2<br>
        &rbrace; else &lbrace;<br>
        ⠀⠀// code block 3<br>
        &rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        For example, to check if a number is positive, negative or zero:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int num = 5;<br>
        if (num &gt 0) &lbrace;<br>
        ⠀⠀System.out.println("The number is positive."); // prints this<br>
        &rbrace; else if (num &lt 0) &lbrace;<br>
        ⠀⠀System.out.println("The number is negative.");<br>
        &rbrace; else &lbrace;<br>
        ⠀⠀System.out.println("The number is zero.");<br>
        &rbrace;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Nested If/Else Expressions</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Nested if/else expressions are used when there are multiple conditions that need to 
        be evaluated in a hierarchical manner. In a nested if/else statement, there is an 
        outer if/else statement that contains an inner if/else statement. An example for a 
        nested if/else statement is as follows:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        if (condition1) &lbrace;<br>
        ⠀⠀if (condition2) &lbrace;<br>
        ⠀⠀⠀⠀// code block 1<br>
        ⠀⠀&rbrace; else &lbrace;<br>
        ⠀⠀⠀⠀// code block 2<br>
        ⠀⠀&rbrace;<br>
        &rbrace; else &lbrace;<br>
        ⠀⠀// code block 3<br>
        &rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        For example, to check if a number is positive, negative, or zero using nested if/else statements:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int num = 5;<br>
        if (num &gt; 0) &lbrace;<br>
        ⠀⠀System.out.println("The number is positive."); // prints this<br>
        &rbrace; else &lbrace;<br>
        ⠀⠀if (num &lt; 0) &lbrace;<br>
        ⠀⠀⠀⠀System.out.println("The number is negative.");<br>
        ⠀⠀&rbrace; else &lbrace;<br>
        ⠀⠀⠀⠀System.out.println("The number is zero.");<br>
        ⠀⠀&rbrace;<br>
        &rbrace;       
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Equivalent Expressions with DeMorgan's Law</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        DeMorgan's Law is a rule in logic that describes how to negate an expression. In Java, 
        DeMorgan's Law can be used to express a Boolean expression in an equivalent form. 
        Some basic rules are:
        <ul class="list-disc pl-8">
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">!(a && b)</Kbd> equal to <Kbd class="px-1.5 py-1 font-mono font-semibold">!a || !b</Kbd></li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">!(a || b)</Kbd> equal to <Kbd class="px-1.5 py-1 font-mono font-semibold">!a && !b</Kbd></li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">!(!a)</Kbd> equal to <Kbd class="px-1.5 py-1 font-mono font-semibold">a</Kbd></li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">!(a == b)</Kbd> equal to <Kbd class="px-1.5 py-1 font-mono font-semibold">a != b</Kbd></li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">!(a != b)</Kbd> equal to <Kbd class="px-1.5 py-1 font-mono font-semibold">a == b</Kbd></li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">!(x &lt; 0)</Kbd> equal to <Kbd class="px-1.5 py-1 font-mono font-semibold">x &gt;= 0</Kbd></li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">!(x &gt; 0)</Kbd> equal to <Kbd class="px-1.5 py-1 font-mono font-semibold">x &lt;= 0</Kbd></li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">!(x &lt;= 0)</Kbd> equal to <Kbd class="px-1.5 py-1 font-mono font-semibold">x &gt; 0</Kbd></li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">!(x &gt;= 0)</Kbd> equal to <Kbd class="px-1.5 py-1 font-mono font-semibold">x &lt; 0</Kbd></li>
        </ul>
        For example, to express the negation of AND using DeMorgan's Law:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int num1 = 5;<br>
        int num2 = 7;<br>
        if (!(num1 &gt; 0 && num2 &gt; 0)) &lbrace; // num1 &lt;= 0 || num2 &lt;= 0<br>
        ⠀⠀System.out.println("At least one number is negative or zero.");<br>
        &rbrace; else &lbrace;<br>
        ⠀⠀System.out.println("Both numbers are positive."); // prints this<br>
        &rbrace;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Comparing Objects</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        In Java, objects can be compared using the equals method. The equals method returns 
        true if the two objects have the same content, and false otherwise. It is important 
        to note that the equals method is not the same as the == operator, which checks if 
        two objects are the same instance.
        <br>
        For example, to compare two string objects:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        String str1 = "Hello";<br>
        String str2 = "World";<br>
        if (str1.equals(str2)) &lbrace; // == checks the memory location, not value of String<br>
        ⠀⠀System.out.println("The strings are equal.");<br>
        &rbrace; else &lbrace;<br>
        ⠀⠀System.out.println("The strings are not equal."); // prints this<br>
        &rbrace;
    </P>

</div>
