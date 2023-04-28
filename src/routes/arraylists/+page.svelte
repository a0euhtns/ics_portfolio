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
    <Heading tag="h2" class="mb-4">ArrayLists</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Introduction to ArrayLists</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        An ArrayList is a collection of data, similar to an array, but with a dynamic size. 
        The size of an ArrayList can be changed, unlike an array where the size is fixed once created. 
        The ArrayList is part of the java.util package, so make sure to import it with 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">import java.util.*;</Kbd> before using it in 
        your program.
    </P>

    <Heading tag="h4" weight="light" class="mb-4">Initializing ArrayLists</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        To initialize an ArrayList, use the following syntax:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        ArrayList&lt;Type&gt; list = new ArrayList&lt;&gt;();
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        where Type is the type of object that you want to store in the ArrayList. You can also 
        instantiate an ArrayList with an existing array, like this:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int[] arr = &lbrace;1, 2, 3, 4, 5&rbrace;;<br>
        ArrayList&lt;Type&gt; list = new ArrayList&lt;&gt;();
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        You can also initially set the size of the ArrayList by specifying an integer in the 
        constructor, like this:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        ArrayList&lt;Integer&gt; list = new ArrayList&lt;&gt;(5);
    </P>
    <Heading tag="h4" weight="light" class="mb-4">ArrayList Methods</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Some of the most commonly used ArrayList methods include:
        <ul class="list-disc pl-8">
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">size()</Kbd> - 
                returns the number of elements in the ArrayList.</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">add(a)</Kbd> - 
                adds the object <Kbd class="px-1.5 py-1 font-mono font-semibold">a</Kbd> 
                to the end of the ArrayList and returns true if the element is added.</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">add(index, a)</Kbd> - 
                inserts the element <Kbd class="px-1.5 py-1 font-mono font-semibold">a</Kbd>
                at the specified index in the ArrayList and shifts everything from index to 
                the right.</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">get(index)</Kbd> - 
                returns the object at the specified index in the ArrayList.</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">set(index, a)</Kbd> - 
                replaces the object at the specified index in the ArrayList with the element 
                <Kbd class="px-1.5 py-1 font-mono font-semibold">a</Kbd> 
                and returns the original element.</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">remove(index)</Kbd> - 
                removes the object at the specified index from the ArrayList and returns it.</li>
        </ul><br>
        When passing an ArrayList into a method, it is passed by reference. This means that when you 
        make changes to the ArrayList inside the method, the changes are made to the original ArrayList. 
        Note that if you pass in an ArrayList without specifying the type, the compiler will give a warning 
        because elements of different types can be added to the ArrayList, resulting in runtime errors.
    </P>

    <Heading tag="h4" weight="light" class="mb-4">Traversing ArrayLists</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        You can traverse an ArrayList using a for loop or a while loop, just like with arrays. 
        You can also use a for-each loop to iterate over the elements in the ArrayList:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        for (Type a : list) &lbrace;<br>
        ⠀⠀// do something with a<br>
        &rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Note that you cannot modify the size of the ArrayList while iterating over it with a for-each loop, 
        or you will get a <Kbd class="px-1.5 py-1 font-mono font-semibold">ConcurrentModificationException</Kbd>. 
        If you need to add or remove elements while iterating over the ArrayList, use a for loop instead.
    </P>
</div>