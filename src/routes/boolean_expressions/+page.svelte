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
    {@html `<pre><code>
Boolean Expressions
Expressions
primitives and references can be compared using relational operators
==, !=
arithmetic values can be compared
<, >, <=, >=
evaluate to boolean values
if - else-if - else
code inside if statement executes if the boolean condition is true
else executes when if is false
else if executes if initial if is false, but else if boolean condition is true
Compound Expressions
nested if statements
logical operators !, &&, ||
order of operations
! flips boolean value
&& satisfied if both are true
|| satisfied if either or both are true
when result can be determined with only 1 boolean operand for &&, ||, second is not evaluated
short-circuited evaluation
Equivalent Expressions
DeMorgan's law
!(a && b) = !a || !b
!(a || b) = !a && !b
!(x < 0) = x >= 0
truth tables
Comparing Objects
object references can be compared
if 2 references are equal, aliases
relational operators can check for null values
implement object equals method
check both values of attributes
    </code></pre>`}
</div>