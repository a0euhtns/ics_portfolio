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