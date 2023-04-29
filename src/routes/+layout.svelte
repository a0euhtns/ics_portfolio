<script>
    import "../app.postcss";
    import * as Flowbite from "flowbite-svelte";
    let btnClass = 'text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 rounded-lg text-xl p-2';
</script>

<slot />
<div class="relative px-8">
    <Flowbite.Navbar
        navClass="px-2 sm:px-4 py-2.5 fixed w-full z-20 top-0 left-0 border-b"
        let:hidden
        let:toggle
        color="red"
        rounded
    >
        <Flowbite.NavBrand href="/">
            <img
                src="https://cdn.discordapp.com/attachments/919393991936606271/1096599855083835452/vector.png"
                class="mr-3 h-6 sm:h-9"
                alt="Logo"
            />
            <span
                class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
                >&lbrace;Felix Zhao&rbrace;</span
            >
        </Flowbite.NavBrand>
        <Flowbite.NavHamburger on:click={toggle} />
        <Flowbite.NavUl {hidden}>
            <Flowbite.NavLi href="/" class="hover:text-red-800">Home</Flowbite.NavLi>
            <Flowbite.NavLi href="/about">About</Flowbite.NavLi>
            <Flowbite.NavLi id="nav-menu1" class="cursor-pointer"
                ><Flowbite.Chevron aligned>Lessons</Flowbite.Chevron
                ></Flowbite.NavLi
            >
            <Flowbite.NavLi href="/projects">Projects</Flowbite.NavLi>
            <Flowbite.NavLi href="/sources">Sources</Flowbite.NavLi>
            <Flowbite.DarkMode {btnClass} />
            <Flowbite.Dropdown triggeredBy="#nav-menu1" class="w-44 z-20">
                <Flowbite.DropdownItem href="/primitives"
                    >Primitives</Flowbite.DropdownItem
                >
                <Flowbite.DropdownItem href="/objects"
                    >Objects</Flowbite.DropdownItem
                >
                <Flowbite.DropdownItem href="/boolean_expressions"
                    >Boolean Expressions</Flowbite.DropdownItem
                >
                <Flowbite.DropdownItem href="/iteration"
                    >Iteration</Flowbite.DropdownItem
                >
                <Flowbite.DropdownItem href="/classes"
                    >Classes</Flowbite.DropdownItem
                >
                <Flowbite.DropdownItem href="/arrays"
                    >Arrays</Flowbite.DropdownItem
                >
                <Flowbite.DropdownItem href="/arraylists"
                    >ArrayLists</Flowbite.DropdownItem
                >
                <Flowbite.DropdownItem href="/searching_and_sorting"
                    >Searching and Sorting</Flowbite.DropdownItem
                >
                <Flowbite.DropdownItem href="/2d_arrays"
                    >2D Arrays</Flowbite.DropdownItem
                >
                <Flowbite.DropdownItem href="/inheritance"
                    >Inheritance</Flowbite.DropdownItem
                >
                <Flowbite.DropdownItem href="/recursion"
                    >Recursion</Flowbite.DropdownItem
                >
            </Flowbite.Dropdown>
        </Flowbite.NavUl>
    </Flowbite.Navbar>
</div>
