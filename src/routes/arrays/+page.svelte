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
    <Heading tag="h2" class="mb-4">Arrays</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Creation</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Arrays are created using the <Kbd class="px-1.5 py-1 font-mono font-semibold">new</Kbd> 
        keyword, which allocates memory for the array and 
        initializes its elements to default values. The size of the array is established at 
        creation and cannot be changed. Arrays can store references to objects or primitive 
        values such as integers or doubles.<br>
        Here is an example of creating an array of integers with size 5:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int[] arr = new int[5];
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        The default initializations for array elements are as follows:
        <ul class="list-disc pl-8">
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">int</Kbd> - 0</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">double</Kbd> - 0.0</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">boolean</Kbd> - false</li>
            <li><Kbd class="px-1.5 py-1 font-mono font-semibold">Reference variables</Kbd> - null</li>
        </ul>
        Initialization lists can also be used to create and initialize an array in a single statement:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int[] arr = &lbrace;1, 2, 3, 4, 5&rbrace;;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Access</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Array elements are accessed using square brackets <Kbd class="px-1.5 py-1 font-mono font-semibold">[]</Kbd>, 
        and their indices range from 0 to <Kbd class="px-1.5 py-1 font-mono font-semibold">length-1</Kbd>. 
        Trying to access an index outside of this range will result in an 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">ArrayIndexOutOfBoundsException</Kbd>. 
        The <Kbd class="px-1.5 py-1 font-mono font-semibold">length</Kbd> of an array can be accessed 
        using the <Kbd class="px-1.5 py-1 font-mono font-semibold">array.length</Kbd> field.<br><br>
        Here is an example of accessing an element in an array:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int value = arr[2]; // retrieves the value at index 2
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Traversal</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        To access all elements in an array, we can use iteration. We must use indexed loops, 
        where elements are accessed by their indices. Care must be taken to ensure that the 
        loop doesn't run for too many or too few iterations (off by one error).<br><br>
        Here is an example of using an indexed loop to traverse an array:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        for (int i = 0; i &lt; arr.length; i++) &lbrace;<br>
        ⠀⠀int value = arr[i]; // do something with value<br>
        &rbrace;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">For-each Loop</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        A for-each loop, also known as an enhanced for loop, can be used to iterate over all 
        elements in an array without using indices. This is a convenient way to traverse 
        arrays and can improve code readability.<br><br>
        Here is an example of using a for-each loop to traverse an array:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        for (int value : arr) &lbrace;<br>
        ⠀⠀// do something with value<br>
        &rbrace;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Algorithms</Heading>
    <Heading tag="h5" weight="light" class="mb-4">Finding the minimum and maximum values in an array</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        To find the minimum or maximum value in an array, follow these steps:
        <ul class="list-decimal pl-8">
            <li>Set the minimum or maximum variable to the first element in the array 
                (e.g., <Kbd class="px-1.5 py-1 font-mono font-semibold">int min = arr[0]</Kbd> 
                or <Kbd class="px-1.5 py-1 font-mono font-semibold">int max = arr[0]</Kbd>).</li>
            <li>Loop through the array from the second element (index 1) to the last element 
                (index <Kbd class="px-1.5 py-1 font-mono font-semibold">arr.length - 1</Kbd>).</li>
            <li>For each element in the array, compare it to the current minimum or maximum value.</li>
            <li>If the element is smaller than the current minimum value, update the minimum variable.</li>
            <li>If the element is larger than the current maximum value, update the maximum variable.</li>
            <li>After traversing the entire array, the minimum or maximum variable will hold the smallest 
                or largest element in the array, respectively.</li>
        </ul><br>
        You can also keep track of the index of the minimum or maximum value by initializing an index variable 
        to 0 and updating it whenever you update the corresponding minimum or maximum variable.
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int[] arr = &lbrace;5, 2, 7, 3, 1&rbrace;;<br><br>

        int min = arr[0];<br>
        int max = arr[0];<br><br>

        for (int i = 1; i &lt; arr.length; i++) &lbrace;<br>
        ⠀⠀if (arr[i] &lt; min) &lbrace;<br>
        ⠀⠀⠀⠀min = arr[i];<br>
        ⠀⠀&rbrace;<br>
        ⠀⠀if (arr[i] &gt; max) &lbrace;<br>
        ⠀⠀⠀⠀ max = arr[i];<br>
        ⠀⠀&rbrace;<br>
        &rbrace;<br><br>

        System.out.println("Minimum value: " + min);<br>
        System.out.println("Maximum value: " + max);
    </P>
    <Heading tag="h5" weight="light" class="mb-4">Calculating the average value of an array</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        To calculate the average value of an array, follow these steps:
        <ul class="list-decimal pl-8">
            <li>Initialize a variable to 0 to store the cumulative sum of all the elements in the array.</li>
            <li>Loop through the array and add each element to the cumulative sum variable.</li>
            <li>After traversing the entire array, divide the cumulative sum variable by the length of the 
                array to get the average value.</li>
        </ul>
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int[] arr = &lbrace;5, 2, 7, 3, 1&rbrace;;<br><br>

        double sum = 0;<br><br>

        for (int i = 0; i &lt; arr.length; i++) &lbrace;<br>
        ⠀⠀sum += arr[i];<br>
        &rbrace;<br><br>

        double average = sum / arr.length;<br><br>

        System.out.println("Average value: " + average);
    </P>
    <Heading tag="h5" weight="light" class="mb-4">Shifting the elements in an array</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        To shift the elements in an array by a specific amount, follow these steps
        <ul class="list-decimal pl-8">
            <li>Make a new array with the same length as the original array to store the final shifted array.</li>
            <li>Loop through the original array and for each element, add the specific shift amount to its index 
                and take the result modulo the length of the array.</li>
            <li>Store the value of the original element in the corresponding index in the new array.</li>
            <li>Repeat steps 2-3 for all elements in the original array.</li>
            <li>The new array will now contain the elements from the original array shifted by the specified amount. 
                To prevent elements from going out of bounds, use the modulo operator to cycle back to the beginning 
                of the array if necessary.</li>
        </ul>
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int[] arr = &lbrace;5, 2, 7, 3, 1&rbrace;;<br><br>

        int shiftAmount = 2;<br>
        int[] shiftedArr = new int[arr.length];<br><br>

        for (int i = 0; i &lt; arr.length; i++) &lbrace;<br>
        ⠀⠀int shiftedIndex = (i + shiftAmount) % arr.length;<br>
        ⠀⠀shiftedArr[shiftedIndex] = arr[i];<br>
        &rbrace;<br><br>

        System.out.println("Original array: " + Arrays.toString(arr));<br>
        System.out.println("Shifted array: " + Arrays.toString(shiftedArr));
    </P>
</div>