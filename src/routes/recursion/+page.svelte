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
    <Heading tag="h2" class="mb-4">Recursion</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Recursive Methods</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        A recursive method is a method that calls itself. It provides an elegant way to solve 
        problems that can be broken down into smaller problems of the same type. In general, 
        a recursive method has two parts: the base case and the recursive case. The base case 
        is the stopping condition of the recursion. It is the case in which the method returns 
        without calling itself. The recursive case is where the method calls itself with smaller 
        inputs, moving towards the base case. Each recursive call has its own set of local variables, 
        different from other calls. Parameter values track recursion, like loop control variables.
        <br><br>

        Recursion can be replicated with iteration, but it is often easier and more intuitive to 
        use recursion in situations that call for it. However, recursion can lead to infinite 
        recursion, which results in a stack overflow. Therefore, it is important to make sure 
        that the base case is well defined and that the recursion will eventually end.
        <br><br>

        Recursion can be used to traverse Strings, arrays, and ArrayLists. The same algorithms 
        that can be used for iteration can be used for recursion, but sometimes recursion can 
        provide a more elegant solution to a problem.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Laws of Recursion</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        <ul class="list-decimal pl-8">
            <li>A recursive method must call itself</li>
            <li>A recursive method must have a base case</li>
            <li>A recursive method must move towards the base case each time it is called</li>
        </ul>
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Tracing Recursion</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Tracing a recursive method involves keeping track of each call in a stack trace. When 
        a recursive method is called, the parameters and local variables for that call are 
        added to the stack. Each subsequent call is added to the top of the stack. Once the 
        base case is reached, the method returns and the call is removed from the stack. 
        The previous call can then resume execution. One way to think about it is like a 
        stack of books, you add a new book to the stack until you reach the base case, which 
        is when you start taking books off of the stack until there are no books left.
    </P>
</div>