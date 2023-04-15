<script>
    import {
        Navbar,
        NavBrand,
        NavLi,
        NavUl,
        NavHamburger,
        Dropdown,
        DropdownItem,
        Chevron,
        P,
    } from "flowbite-svelte";
</script>

<div class="relative px-8">
    <Navbar
        navClass="px-2 sm:px-4 py-2.5 fixed w-full z-20 top-0 left-0 border-b"
        let:hidden
        let:toggle
        color="red"
        rounded
    >
        <NavBrand href="/">
            <img
                src="https://cdn.discordapp.com/attachments/919393991936606271/1096599855083835452/vector.png"
                class="mr-3 h-6 sm:h-9"
                alt="Logo"
            />
            <span
                class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
                >Felix Zhao</span
            >
        </NavBrand>
        <NavHamburger on:click={toggle} />
        <NavUl {hidden}>
            <NavLi href="/">Home</NavLi>
            <NavLi href="/about">About</NavLi>
            <NavLi id="nav-menu1" class="cursor-pointer" active={true}
                ><Chevron aligned>Lessons</Chevron></NavLi
            >
            <NavLi href="/projects">Projects</NavLi>
            <NavLi href="/sources">Sources</NavLi>
            <Dropdown triggeredBy="#nav-menu1" class="w-44 z-20">
                <DropdownItem href="/primitives">Primitives</DropdownItem>
                <DropdownItem href="/objects">Objects</DropdownItem>
                <DropdownItem href="/boolean_expressions"
                    >Boolean Expressions</DropdownItem
                >
                <DropdownItem href="/iteration">Iteration</DropdownItem>
                <DropdownItem href="/classes">Classes</DropdownItem>
                <DropdownItem href="/arrays">Arrays</DropdownItem>
                <DropdownItem href="/arraylists">ArrayLists</DropdownItem>
                <DropdownItem href="/2d_arrays">2D Arrays</DropdownItem>
                <DropdownItem href="/inheritance">Inheritance</DropdownItem>
                <DropdownItem href="/recursion">Recursion</DropdownItem>
            </Dropdown>
        </NavUl>
    </Navbar>
</div>
<div class="pt-20">
    <P weight="light" color="text-gray-500 dark:text-gray-400">
        Primitive Variables Printing check spelling of the print statement check
        number of double quotes, syntax error Variables and Data Types Primitive
        boolean - true/false int - 32 bit integers double - decimal numbers
        Non-primitive Strings - text defined with double quotes most
        non-primitive variables are made by the user Variable Names letters,
        digits or underscores may not start with a digit spaces are not allowed
        no java reserved words camelCase Constants use the word “final” before
        the data type and identifier constants should be UPPER_CASE with
        underscores Arithmetic Expressions ORDER OF OPERATIONS String literals
        are surrounded by double quotes, can only concatenate to them addition
        subtraction multiplication / division integer division removes decimal
        divide by 0 - ArithmeticException % modulus remainder mod has same order
        as * and / Assignment Operator = assigns the value on the right side to
        the variable on the left assignment is last in order of operations
        compound assignment operators += -= *= /= %= Increment and Decrement ++
        increment += 1 -- decrement = 1 Casting change the type of one variable
        to another from larger data type to smaller, loss of data (double) 1/6;
        makes 1 into double always casts right after Integer max
        Integer.MAX_VALUE; Integer.MIN_VALUE; integer overflow
    </P>
</div>
