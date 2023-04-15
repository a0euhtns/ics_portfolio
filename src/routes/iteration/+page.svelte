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
Iteration
While


iterates 0 or more times


exits loop if boolean expression is false


infinite loop if boolean expression is always true


never executes if boolean expression is initially false


Algorithms

 //divisible by another integer
if (a % b == 0) //code

//individual digit sum
int num = 1232;
int sum = 0;
while (num > 0) {
		sum += num % 10;
		num /= 10;
}

//interest
int years = 0;
double cur = 200.0;
double total = 1000.0;
double interest = 0.1;
while (cur < total) {
		cur += cur*interest;
		years++;
}


For


initialization, check, body, update


initialization only executed once
update after loop body, checks before iterating again
example

 for (int i = 0; i < n; i++) {
		System.out.println(i);
)


ends when check is false


for loops can be written into while loops


“off by one” errors, loops don’t run as many times as they are supposed to


String Algorithms


contains example

String str = "sunflower";
String check = "lower";
boolean found = false;
for (int i = 0; i <= str.length()-check.length(); i++) {
	String portion = str.substring(i, i+check.length());
	if (portion.equals(check)) found = true;
}


NO charAT(), only substring(i, i+1);


Nested


inner loop must complete all iterations before outer loop continues
inner loop based on outer loop, each time outer loop increments inner loop increments more times
Informal Code Analysis


statement execution count
number of times the statement executes in a loop
informal runtime
total number of loops is inside * outside
    </code></pre>`}
</div>