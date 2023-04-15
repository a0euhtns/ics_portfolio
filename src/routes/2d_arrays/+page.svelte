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
## 2D Arrays

- 2D Array Creation
    - 2d arrays represent collections of data in 2 dimensions
        - array of arrays
    - indices are represented the same
        - row, then column
    - initializer array
        - multiple initializer lists, each representing 1d arrays
        - int[][] arr = {{1,2}, {2,3}};
    - arr[row][col] are used to access and modify a specific element
- Traversing 2D Arrays
    - nested iteration statements to access all elements
        - loop through all rows, looping through each column at each row
    - for-each loops
        - outside loops through rows, inside loops through elements in row
            
            for (int[] x : arr) {
            	for (int y : x) {
            		//body
            	}
            }
            
    - iteration can be written with row-major or column-major order
        - row-major: loop through rows on outside loop, columns on inner loop
        - column-major: loop through columns on outside loop, rows on inner loop
        
        for (int c = 0; c < arr[0].length; c++) {
        	for (int r = 0; r < arr.length; r++) {
        		System.out.println(arr[r][c]);
        	}
        }
        
    - All algorithms for 1d arrays work for 2d arrays
        - linear search: search through all elements 1 row at a time
    </code></pre>`}
</div>