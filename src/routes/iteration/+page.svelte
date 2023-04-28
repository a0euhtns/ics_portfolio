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