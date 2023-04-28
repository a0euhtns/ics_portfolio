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