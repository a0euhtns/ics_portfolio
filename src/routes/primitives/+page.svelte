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
    } from "flowbite-svelte";
</script>

<div class="pt-20">
    <Heading tag="h2" class="mb-4">Primitive Variables</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Primitive Data Types</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4">
        Java has eight primitive data types, which are divided into four
        categories: integer, floating-point, character, and boolean.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Integer Types</Heading>
    <Table>
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
    <Table>
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
    <Table>
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
    <Table>
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
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4">
        To declare a primitive variable, you need to specify its data type and a name. For example:
    </P>
</div>
