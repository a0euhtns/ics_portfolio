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
    <Heading tag="h2" class="mb-4">Primitive Variables</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Primitive Data Types</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Java has eight primitive data types, which are divided into four
        categories: integer, floating-point, character, and boolean.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Integer Types</Heading>
    <Table class="mb-4">
        <TableHead>
            <TableHeadCell>Type</TableHeadCell>
            <TableHeadCell>Size (bits)</TableHeadCell>
            <TableHeadCell>Range</TableHeadCell>
        </TableHead>
        <TableBody>
            <TableBodyRow>
                <TableBodyCell>byte</TableBodyCell>
                <TableBodyCell>8</TableBodyCell>
                <TableBodyCell>-128 to 127</TableBodyCell>
            </TableBodyRow>
            <TableBodyRow>
                <TableBodyCell>short</TableBodyCell>
                <TableBodyCell>16</TableBodyCell>
                <TableBodyCell>-32,768 to 32,767</TableBodyCell>
            </TableBodyRow>
            <TableBodyRow>
                <TableBodyCell>int</TableBodyCell>
                <TableBodyCell>32</TableBodyCell>
                <TableBodyCell>-2,147,483,648 to 2,147,483,647</TableBodyCell>
            </TableBodyRow>
            <TableBodyRow>
                <TableBodyCell>long</TableBodyCell>
                <TableBodyCell>64</TableBodyCell>
                <TableBodyCell>-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807</TableBodyCell>
            </TableBodyRow>
        </TableBody>
    </Table>
    <Heading tag="h4" weight="light" class="mb-4">Floating-Point Types</Heading>
    <Table class="mb-4">
        <TableHead>
            <TableHeadCell>Type</TableHeadCell>
            <TableHeadCell>Size (bits)</TableHeadCell>
            <TableHeadCell>Range</TableHeadCell>
            <TableHeadCell>Precision (decimals)</TableHeadCell>
        </TableHead>
        <TableBody>
            <TableBodyRow>
                <TableBodyCell>float</TableBodyCell>
                <TableBodyCell>32</TableBodyCell>
                <TableBodyCell>1.4E-45 to 3.4028235E38</TableBodyCell>
                <TableBodyCell>6-7</TableBodyCell>
            </TableBodyRow>
            <TableBodyRow>
                <TableBodyCell>double</TableBodyCell>
                <TableBodyCell>64</TableBodyCell>
                <TableBodyCell>4.9E-324 to 1.7976931348623157E308</TableBodyCell>
                <TableBodyCell>15-16</TableBodyCell>
            </TableBodyRow>
        </TableBody>
    </Table>
    <Heading tag="h4" weight="light" class="mb-4">Character Type</Heading>
    <Table class="mb-4">
        <TableHead>
            <TableHeadCell>Type</TableHeadCell>
            <TableHeadCell>Size (bits)</TableHeadCell>
            <TableHeadCell>Range</TableHeadCell>
        </TableHead>
        <TableBody>
            <TableBodyRow>
                <TableBodyCell>char</TableBodyCell>
                <TableBodyCell>16</TableBodyCell>
                <TableBodyCell>'\u0000' (0) to '\uffff' (65,535)</TableBodyCell>
            </TableBodyRow>
        </TableBody>
    </Table>
    <Heading tag="h4" weight="light" class="mb-4">Boolean Type</Heading>
    <Table class="mb-4">
        <TableHead>
            <TableHeadCell>Type</TableHeadCell>
            <TableHeadCell>Size (bits)</TableHeadCell>
            <TableHeadCell>Range</TableHeadCell>
        </TableHead>
        <TableBody>
            <TableBodyRow>
                <TableBodyCell>boolean</TableBodyCell>
                <TableBodyCell>1</TableBodyCell>
                <TableBodyCell>true or false</TableBodyCell>
            </TableBodyRow>
        </TableBody>
    </Table>
    <Heading tag="h4" weight="light" class="mb-4">Declaring Variables</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        To declare a primitive variable, you need to specify its data type and a name.<br>For example:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int age;<br>
        double weight;<br>
        char initial;<br>
        boolean isStudent;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Initializing Variables</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        When a variable is declared, it does not have a value. You need to assign a value to it before you can use it. You can initialize a variable when you declare it, or later in the code.<br>For example:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int age = 18;<br>
        double weight = 68.5;<br>
        char initial = 'J';<br>
        boolean isStudent = true;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Type Conversion</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Java has strict rules for type conversion. When you assign a value of one type to a variable of another type, the value may be automatically converted to the target type.<br>For example:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        int a = 5;<br>
        double b = a; // automatic conversion from int to double
    </P>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        However, some conversions may result in a loss of precision or truncation of data. You can use explicit type casting to convert a value to a different type.<br>For example:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        double x = 3.14;
        int y = (int) x; // explicit casting from double to int
    </P>
</div>
