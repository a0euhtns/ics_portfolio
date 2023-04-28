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