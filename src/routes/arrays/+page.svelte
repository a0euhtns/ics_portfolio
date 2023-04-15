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
<div class="pt-16">
    {@html `<pre><code>
Arrays
Creation
arrays represent multiple values with a single variable
can store references
size is established and cannot be changed
created using new
int[] arr = new int[5];
default initializations:
int - 0
double - 0.0
boolean - false
references - null
initialization lists can be used
int[] arr = {1, 2, 3, 4, 5};
Access
square brackets are used to access and modify array
values range from 0 to length-1
values outside return ArrayIndexOutOfBoundsException
access length through arr.length
Traversal
iteration can be used to access all elements in the array
loop from 0 to length-1
must use indexed loops, elements are accessed by indicies
be careful of the number of times you loop, “off by one”
For-each Loop
aka enhanced for loop
does not use indexes, only gets value at the index in array
2 parts
type and name of the value in the data structure
data structure being traversed
parts separated by colon
in the body you can access the value stored in the variable initialized in first part
for (int x : arr)
Algorithms
min/max
set min/max variable to first element (arr[0])
loop through 1 to length-1
if current is smaller/bigger than the min/max, set min/max
after traversing the entire array, you will have the largest/smallest element in the array
can have a min/max index, set as 0 in the beginning
update index = i whenever you update min/max
average
have a variable that stores the cumulative sum as you traverse the array
divide the variable by length
shifting array
make a new array to store the final shifted array
each element, add a specific amount shifted and mod by length
cycle back, prevent elements from going out of bounds
    </code></pre>`}
</div>