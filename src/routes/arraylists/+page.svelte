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
## ArrayList

- Initialize ArrayLists
    - **********************part of java.util, import java.util.*;**********************
    - collection of data, like arrays
    - size can change
    - ArrayList<Type> = new ArrayList<>();
        - could also be instantiated, new ArrayList<>(arr);
    - can initially set size of arraylist, new ArrayList<>(5);
- ArrayList Methods
    - size() size of ArrayList
    - add(a) adds to the end
    - add(index, a) adds at the index
    - get(index) gets element at index
    - set(index, a) sets element at index
    - remove(index) removes element at index
    - when you pass ArrayList into a method, passes by reference
        - when you edit in method, edits the original list
        - passing in ArrayList instead of ArrayList<Type> gives unchecked warning
            - elements are able to be added that are not the same type, compiler gives warning
- Traversing ArrayLists
    - same as arrays for for and while loops
    - for-each: for (type a : list)
        - changing size in enhanced for loop gives ConcurrentModificationException
        - don't add or remove elements
    - when checking if 2 objects are equal, obj.equals(object)
    </code></pre>`}
</div>