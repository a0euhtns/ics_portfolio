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
    <Heading tag="h2" class="mb-4">Iteration</Heading>
    <Heading tag="h4" weight="light" class="mb-4">While Loops</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        A while loop is used when you need to repeat a block of code while a certain condition is true. 
        The condition is tested before the code in the loop is executed. If the condition is true, the 
        code is executed, and then the condition is tested again. This process continues until the 
        condition becomes false.
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        while (condition) &lbrace;<br>
        ⠀⠀// code to be executed<br>
        &rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        An example of an algorithm that uses a while loop is finding the sum of all digits:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int num = 1232;<br>
        int sum = 0;<br>
        while (num &gt; 0) &lbrace;<br>
        ⠀⠀sum += num % 10;<br>
        ⠀⠀num /= 10;<br>
        &rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        In this example, the loop gets the last digit of the number and removes it, 
        continuing until the number reaches 0.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">For Loops</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        A for loop is used when you need to execute a block of code a fixed number of times. 
        The number of times the loop is executed is determined by the loop control variable, 
        which is usually an integer.
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        for (initialization; condition; update) &lbrace;<br>
        ⠀⠀// code to be executed<br>
        &rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        This is an example of a for loop which prints numbers from 1 to n:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        for (int i = 0; i &lt;= n; i++) &lbrace;<br>
        ⠀⠀System.out.println(i);<br>
        &rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        An example of an algorithm that uses a for loop is for calculating interest:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int years = 10;<br>
        double money = 200.0;<br>
        double interest = 0.1;<br>
        for (int i = 0; i &lt; years; i++) &lbrace;<br>
        ⠀⠀money += money * interest;<br>
        &rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        In this example, the loop calculates the total price after a certain number of years, 
        with the interest percentage as a decimal.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Nested Loops</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Nested loops are loops that are placed inside other loops. They are used when you 
        need to iterate over a two-dimensional data structure, such as a 2D array.
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        for (int i = 0; i &lt; rows; i++) &lbrace;<br>
        ⠀⠀for (int j = 0; j &lt; columns; j++) &lbrace;<br>
        ⠀⠀⠀⠀// code to be executed<br>
        ⠀⠀&rbrace;<br>
        &rbrace;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Informal Code Analysis</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Before running a program, you can perform an informal code analysis to estimate the 
        runtime and execution count of different statements. This can help you identify 
        potential bottlenecks or inefficiencies in your code. One of the ways to calculate 
        your execution count for nested loops is to multiply the number of times the outside 
        loop runs by the number of times the inside loop runs.
    </P>
</div>