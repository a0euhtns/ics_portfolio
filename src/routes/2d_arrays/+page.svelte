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