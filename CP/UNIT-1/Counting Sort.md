# Counting Sort

- It is a non-comparision based sorting algorithm, in which we use the frequencies of elements in an array to sort them.
- Counting sort is faster than quick sort/merge sort.
- It is used for numbers within small ranges.
- Time complexity : O(n loglogn)
- Space Complexity : O(n+k)


```java
public class CountingSort {

    // Function to perform counting sort
    static void countingSort(int[] arr) {
        int n = arr.length;

        // 1. Find the maximum element
        int max = arr[0];
        for (int i = 1; i < n; i++) {
            if (arr[i] > max) {
                max = arr[i];
            }
        }

        // 2. Create count array
        int[] count = new int[max + 1];
        for (int i = 0; i < n; i++) {
            count[arr[i]]++;
        }

        // 3. Build output array
        int index = 0;
        for (int i = 0; i <= max; i++) {
            while (count[i] > 0) {
                arr[index] = i;
                index++;
                count[i]--;
            }
        }
    }

    // Helper function to print array
    static void printArray(int[] arr) {
        for (int num : arr) {
            System.out.print(num + " ");
        }
        System.out.println();
    }

    // Driver code
    public static void main(String[] args) {
        int[] arr = {4, 2, 2, 8, 3, 3, 1};

        System.out.println("Original Array:");
        printArray(arr);

        countingSort(arr);

        System.out.println("Sorted Array:");
        printArray(arr);
    }
}
```
