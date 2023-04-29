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
    <Heading tag="h2" class="mb-4">2D Arrays</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Creating 2D Arrays</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        To create a 2D array, we use the same syntax as a 1D array, but with an additional 
        set of square brackets. For example, 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">int[][] matrix = new int[3][4];</Kbd> 
        creates a 2D array with three rows and four columns. We can also use an initializer list 
        to create a 2D array: 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">int[][] matrix = &lbrace;&lbrace;1, 2&rbrace;, &lbrace;3, 4&rbrace;, &lbrace;5, 6&rbrace;&rbrace;;</Kbd> 
        creates a 2D array with three rows and two columns, where the first row contains the 
        values 1 and 2, the second row contains 3 and 4, and the third row contains 5 and 6.
        <br><br>

        To access a specific element in a 2D array, we use the syntax 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">matrix[row][column]</Kbd>, 
        where <Kbd class="px-1.5 py-1 font-mono font-semibold">row</Kbd> 
        is the index of the row and <Kbd class="px-1.5 py-1 font-mono font-semibold">column</Kbd> 
        is the index of the column. For example, 
        <Kbd class="px-1.5 py-1 font-mono font-semibold">matrix[1][2]</Kbd> would access the 
        element in the second row and third column.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Traversing 2D Arrays</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        There are several ways to traverse a 2D array. One way is to use nested loops, where 
        the outer loop iterates over the rows and the inner loop iterates over the columns. 
        For example, to print all the elements in a 2D array, we can use the following code:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        for (int i = 0; i &lt; matrix.length; i++) &lbrace;<br>
        ⠀⠀for (int j = 0; j &lt; matrix[i].length; j++) &lbrace;<br>
        ⠀⠀⠀⠀System.out.print(matrix[i][j] + " ");<br>
        ⠀⠀&rbrace;<br>
        ⠀⠀System.out.println();<br>
        &rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Alternatively, we can use a for-each loop to iterate over the rows and columns:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        for (int[] row : matrix) &lbrace;<br>
        ⠀⠀for (int element : row) &lbrace;<br>
        ⠀⠀⠀⠀System.out.print(element + " ");<br>
        ⠀⠀&rbrace;<br>
        ⠀⠀System.out.println();<br>
        &rbrace;
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Finally, we can also traverse a 2D array in column-major order by iterating over the 
        columns in the outer loop and the rows in the inner loop:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        for (int j = 0; j &lt; matrix.length[0]; j++) &lbrace;<br>
        ⠀⠀for (int i = 0; i &lt; matrix.length; i++) &lbrace;<br>
        ⠀⠀⠀⠀System.out.print(matrix[i][j] + " ");<br>
        ⠀⠀&rbrace;<br>
        ⠀⠀System.out.println();<br>
        &rbrace;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Manipulating 2D Arrays</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        All algorithms that work for 1D arrays also work for 2D arrays. For example, we can use 
        linear search to search for a specific element in a 2D array. To search for an element 
        in a 2D array, we can use the following code:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public boolean contains(int[][] matrix, int target) &lbrace;<br>
        ⠀⠀for (int i = 0; i &lt; matrix.length; i++) &lbrace;<br>
        ⠀⠀⠀⠀for (int j = 0; j &lt; matrix[i].length; j++) &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀if (matrix[i][j] == target) &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀⠀⠀return true;<br>
        ⠀⠀⠀⠀⠀⠀&rbrace;<br>
        ⠀⠀⠀⠀&rbrace;<br>
        ⠀⠀&rbrace;<br>
        ⠀⠀return false;<br>
        &rbrace;
    </P>
</div>