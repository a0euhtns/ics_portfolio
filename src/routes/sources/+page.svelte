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
        Kbd,
        NavLi
    } from "flowbite-svelte";
</script>

<div class="pt-20 m-10 mx-36 min-h-screen">
    <Heading tag="h2" class="mb-4">Sources</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Sites Used:</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        <ul class="list-disc pl-8">
            <NavLi href="https://www.w3schools.com/" class="text-blue-500 text-lg">W3 Schools</NavLi>
            <NavLi href="https://www.geeksforgeeks.org/" class="text-blue-500 text-lg">Geeks for Geeks</NavLi>
            <NavLi href="https://kit.svelte.dev/docs/" class="text-blue-500 text-lg">SvelteKit Docs</NavLi>
            <NavLi href="https://flowbite-svelte.com/" class="text-blue-500 text-lg">Flowbite Svelte</NavLi>
        </ul>
    </P>
</div>