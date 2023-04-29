<script>
    import {
        Heading,
        P,
        A,
        Mark,
        Secondary,
        Table,
        TableBody,
        TableBodyCell,
        TableBodyRow,
        TableHead,
        TableHeadCell,
        Checkbox,
        TableSearch,
        Kbd
    } from "flowbite-svelte";
</script>

<div class="pt-20 m-10 mx-36">
    <Heading tag="h2" class="mb-4">Searching and Sorting</Heading>
    <Heading tag="h4" weight="light" class="mb-4">Searching</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Searching is the process of finding a specific element or value in a data structure 
        such as an array or a list. There are several searching algorithms, including linear 
        search and binary search. Linear search is the simplest search algorithm, but it can 
        be inefficient for large data sets. Binary search, on the other hand, is more efficient 
        and works well for large data sets.
    </P>
    <Heading tag="h5" weight="light" class="mb-4">Linear Search</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Linear search is a simple algorithm that searches for an element in an array or list by 
        checking each element one by one. It starts at the beginning of the array and checks each 
        element until it finds the element it's looking for or reaches the end of the array. 
        If the element is found, the algorithm returns the index of the element; otherwise, 
        it returns -1 to indicate that the element was not found.<br><br>

        Here's a short implementation of linear search in Java:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public int linearSearch(int[] arr, int target) &lbrace;<br>
        ⠀⠀for (int i = 0; i &lt; arr.length; i++) &lbrace;<br>
        ⠀⠀⠀⠀if (arr[i] == target) &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀return i;<br>
        ⠀⠀⠀⠀&rbrace;<br>
        ⠀⠀&rbrace;<br>
        ⠀⠀return -1;<br>
        &rbrace;
    </P>
    <Heading tag="h5" weight="light" class="mb-4">Binary Search</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Binary search is a more efficient algorithm that works by dividing the array or list in half repeatedly 
        until it finds the element it's looking for. It requires the data to be sorted in ascending or descending 
        order.<br><br>

        The algorithm starts in the middle of the array and compares the target element to the middle element. 
        If the target is less than the middle element, it searches the left half of the array; otherwise, 
        it searches the right half. It repeats this process on the remaining half until the element is found or the 
        remaining half has no elements left to search.<br><br>

        Here's a short implementation of iterative binary search in Java:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public int binarySearch(int[] arr, int target) &lbrace;<br>
        ⠀⠀int low = 0;<br>
        ⠀⠀int high = arr.length - 1;<br>
        ⠀⠀while (low &lt;= high) &lbrace;<br>
        ⠀⠀⠀⠀int mid = (low + high) / 2;<br><br>

        ⠀⠀⠀⠀if (arr[mid] == target) &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀return mid;<br>
        ⠀⠀⠀⠀&rbrace; else if (arr[mid] &lt; target) &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀low = mid + 1;<br>
        ⠀⠀⠀⠀&rbrace; else &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀high = mid - 1;<br>
        ⠀⠀⠀⠀&rbrace;<br>
        ⠀⠀&rbrace;<br>
        ⠀⠀return -1;<br>
        &rbrace;
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Sorting</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Sorting is the process of arranging the elements of a data structure in a specific order, 
        such as ascending or descending order. There are several sorting algorithms, including 
        selection sort, insertion sort, merge sort, and quicksort. Each algorithm has its own 
        advantages and disadvantages in terms of speed and memory usage.
    </P>
    <Heading tag="h5" weight="light" class="mb-4">Selection Sort</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Selection sort is a simple sorting algorithm that works by repeatedly finding the 
        minimum element from an unsorted part of the array and moving it to the front. The 
        algorithm maintains two subarrays, one that is sorted and one that is unsorted. 
        The sorted subarray is initially empty, and the unsorted subarray is the entire array. 
        In each iteration of the algorithm, the minimum element from the unsorted subarray is 
        found and swapped with the first element of the unsorted subarray. The size of the 
        unsorted subarray is decreased by one in each iteration. The time complexity of selection 
        sort is O(n^2), while the best case scenario is O(n).<br><br>

        Here's an implementation of selection sort in Java:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public void selectionSort(int[] arr) &lbrace;<br>
        ⠀⠀for (int i = 0; i &lt; arr.length - 1; i++) &lbrace;<br>
        ⠀⠀⠀⠀int minIndex = i;<br>
        ⠀⠀⠀⠀for (int j = i + 1; j &lt; arr.length; j++) &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀if (arr[j] &lt; arr[minIndex]) &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀⠀⠀minIndex = j;<br>
        ⠀⠀⠀⠀⠀⠀&rbrace;<br>
        ⠀⠀⠀⠀&rbrace;<br>
        ⠀⠀⠀⠀int temp = arr[i];<br>
        ⠀⠀⠀⠀arr[i] = arr[minIndex];<br>
        ⠀⠀⠀⠀arr[minIndex] = temp;<br>
        ⠀⠀&rbrace;<br>
        &rbrace;
    </P>
    <Heading tag="h5" weight="light" class="mb-4">Insertion Sort</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Insertion sort is a simple sorting algorithm where the list is divided into two parts - 
        sorted and unsorted. Initially, the sorted part contains only the first element of the 
        list and the unsorted part contains the remaining elements. In each iteration, the first 
        element of the unsorted part is taken and compared with the elements in the sorted part. 
        If the element is smaller than the sorted element, then it is moved to the left of the 
        sorted element. This process is repeated until the entire list is sorted. The time complexity 
        of insertion sort is O(n^2), while the best case scenario is O(n).<br><br>

        Here's an implementation of insertion sort in Java:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public void insertionSort(int[] arr) &lbrace;<br>
        ⠀⠀for (int i = 1; i &lt; arr.length; i++) &lbrace;<br>
        ⠀⠀⠀⠀int key = arr[i];<br>
        ⠀⠀⠀⠀int j = i - 1;<br>
        ⠀⠀⠀⠀while (j &gt;= 0 && arr[j] &gt; key) &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀arr[j + 1] = arr[j];<br>
        ⠀⠀⠀⠀⠀⠀j--;<br>
        ⠀⠀⠀⠀&rbrace;<br>
        ⠀⠀⠀⠀arr[j + 1] = key;<br>
        ⠀⠀&rbrace;<br>
        &rbrace;
    </P>
    <Heading tag="h5" weight="light" class="mb-4">Bubble Sort</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Bubble sort is a simple sorting algorithm that works by repeatedly swapping adjacent 
        elements if they are in the wrong order. The algorithm repeatedly traverses the array, 
        comparing adjacent elements and swapping them if they are in the wrong order. The 
        algorithm then moves on to the next pair of adjacent elements and repeats the process 
        until no more swaps are needed.<br><br>

        Bubble sort has a worst-case and average time complexity of O(n^2), making it inefficient 
        for larger arrays. However, it has a best-case time complexity of O(n), making it a good 
        choice for small lists that are nearly sorted.
        <br><br>

        Here's an implementation of bubble sort in Java:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public void bubbleSort(int[] arr) lbrace;<br>
        ⠀⠀int n = arr.length;<br>
        ⠀⠀for (int i = 0; i &lt; n-1; i++) lbrace;<br>
        ⠀⠀⠀⠀for (int j = 0; j &lt; n-i-1; j++) lbrace;<br>
        ⠀⠀⠀⠀⠀⠀if (arr[j] &gt; arr[j+1]) lbrace;<br>
        ⠀⠀⠀⠀⠀⠀⠀⠀// swap arr[j] and arr[j+1]<br>
        ⠀⠀⠀⠀⠀⠀⠀⠀int temp = arr[j];<br>
        ⠀⠀⠀⠀⠀⠀⠀⠀arr[j] = arr[j+1];<br>
        ⠀⠀⠀⠀⠀⠀⠀⠀arr[j+1] = temp;<br>
        ⠀⠀⠀⠀⠀⠀&rbrace;<br>
        ⠀⠀⠀⠀&rbrace;<br>
        ⠀⠀&rbrace;<br>
        &rbrace;
    </P>
    <Heading tag="h5" weight="light" class="mb-4">Merge Sort</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Merge sort is a more efficient sorting algorithm that works by dividing the array into 
        two halves, sorting each half recursively, and then merging the two sorted halves back 
        together. The basic idea behind merge sort is to keep dividing the array in half until 
        the subarrays are trivially sorted (i.e. have length one or zero), and then merge the 
        sorted subarrays back together in a bottom-up fashion. Because of this, the time 
        complexity for merge sort is O(nlogn) no matter the original configuration.
        <br><br>

        Here's an implementation of merge sort in Java:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public void mergeSort(int[] arr, int left, int right) &lbrace;<br>
        ⠀⠀if (left &lt; right) &lbrace;<br>
        ⠀⠀⠀⠀int mid = (left + right) / 2;<br>
        ⠀⠀⠀⠀mergeSort(arr, left, mid);<br>
        ⠀⠀⠀⠀mergeSort(arr, mid + 1, right);<br>
        ⠀⠀⠀⠀merge(arr, left, mid, right);<br>
        ⠀⠀&rbrace;<br>
        &rbrace;<br><br>

        public void merge(int[] arr, int left, int mid, int right) &lbrace;<br>
        ⠀⠀int[] temp = new int[right - left + 1];<br>
        ⠀⠀int i = left, j = mid + 1, k = 0;<br>
        ⠀⠀while (i &lt;= mid && j &lt;= right) &lbrace;<br>
        ⠀⠀⠀⠀if (arr[i] &lt; arr[j]) &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀temp[k++] = arr[i++];<br>
        ⠀⠀⠀⠀&rbrace; else &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀temp[k++] = arr[j++];<br>
        ⠀⠀⠀⠀&rbrace;<br>
        ⠀⠀&rbrace;<br>
        ⠀⠀while (i &lt;= mid) &lbrace;<br>
        ⠀⠀⠀⠀temp[k++] = arr[i++];<br>
        ⠀⠀&rbrace;<br>
        ⠀⠀while (j &lt;= right) &lbrace;<br>
        ⠀⠀⠀⠀temp[k++] = arr[j++];<br>
        ⠀⠀&rbrace;<br>
        ⠀⠀for (int m = 0; m &lt; temp.length; m++) &lbrace;<br>
        ⠀⠀⠀⠀arr[left + m] = temp[m];<br>
        ⠀⠀&rbrace;<br>
        &rbrace;
    </P>
    <Heading tag="h5" weight="light" class="mb-4">Quick Sort</Heading>
    <P weight="light" color="text-gray-500 dark:text-gray-400" class="mb-4 leading-loose">
        Quick sort is a sorting algorithm that follows the divide-and-conquer approach. 
        The algorithm works by selecting a "pivot" element from the array and partitioning 
        the other elements into two sub-arrays, according to whether they are less than or 
        greater than the pivot. The sub-arrays are then recursively sorted.
        <br><br>

        The key to the efficiency of quick sort is the partitioning step. A typical implementation 
        of the partitioning algorithm involves selecting the rightmost element of the array as the 
        pivot, and then scanning through the array, swapping elements as necessary so that all elements 
        less than the pivot are to the left of it, and all elements greater than the pivot are to the 
        right of it.
        <br><br>

        Quick sort has an average and best-case time complexity of O(nlogn), making it a good choice 
        for large lists. However, it has a worst-case time complexity of O(n^2), which occurs when 
        the pivot selected is always the largest or smallest element in the array.
        <br><br>

        Here's an implementation of quick sort in Java:
    </P>
    <P class="text-m p-2 font-mono font-semibold text-gray-800 bg-gray-100 border border-gray-200 rounded-lg dark:bg-gray-600 dark:text-gray-100 dark:border-gray-500 mb-4">
        public static void quickSort(int[] arr, int low, int high) &lbrace;<br>
        ⠀⠀if (low &lt; high) &lbrace;<br>
        ⠀⠀⠀⠀int pivotIndex = partition(arr, low, high);<br>
        ⠀⠀⠀⠀quickSort(arr, low, pivotIndex-1);<br>
        ⠀⠀⠀⠀quickSort(arr, pivotIndex+1, high);<br>
        ⠀⠀&rbrace;<br>
        &rbrace;<br><br>

        public static int partition(int[] arr, int low, int high) &lbrace;<br>
        ⠀⠀int pivot = arr[high];<br>
        ⠀⠀int i = low - 1;<br>
        ⠀⠀for (int j = low; j &lt;= high-1; j++) &lbrace;<br>
        ⠀⠀⠀⠀if (arr[j] &lt;= pivot) &lbrace;<br>
        ⠀⠀⠀⠀⠀⠀i++;<br>
        ⠀⠀⠀⠀⠀⠀int temp = arr[i];<br>
        ⠀⠀⠀⠀⠀⠀arr[i] = arr[j];<br>
        ⠀⠀⠀⠀⠀⠀arr[j] = temp;<br>
        ⠀⠀⠀⠀&rbrace;<br>
        ⠀⠀&rbrace;<br>
        ⠀⠀int temp = arr[i+1];<br>
        ⠀⠀arr[i+1] = arr[high];<br>
        ⠀⠀arr[high] = temp;<br>
        ⠀⠀return i+1;<br>
        &rbrace;
    </P>
</div>