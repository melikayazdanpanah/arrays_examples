# arrays_examples

input an array:

```c
#include <stdio.h>

int main() {
    int n;

    // Number of elements in the first array
    printf("Enter the number of elements for the first array: ");
    scanf("%d", &n);

    int array1[n]
    printf("Enter the elements of the first array:\n");
    for (int i = 0; i < n; i++)
        scanf("%d", &array1[i]);

    // Number of elements in the second array
    printf("Enter the number of elements for the second array: ");
    scanf("%d", &n);

    int array2[n];
    printf("Enter the elements of the second array:\n");
    for (int i = 0; i < n; i++)
        scanf("%d", &array2[i]);

    // Print arrays
    printf("First array:\n ");
    for (int i = 0; i < n; i++)
        printf("%d ", array1[i]);

    printf("\nSecond array:\n ");
    for (int i = 0; i < n; i++)
        printf("%d ", array2[i]);
```

output:
Enter the number of elements for the first array: 
3
Enter the elements of the first array:
1
2
3
Enter the number of elements for the second array:
2
Enter the elements of the second array:
23
45
First array:
1 2 3
Second array:
23 45




insert data to the first array:
```c

int newData;
    printf("Enter a new number to insert into the first array:\n");
    scanf("%d", &newData);

// Insert data into the first array
    array1[n] = newdata;
    n++;

    // Print the first array with the inserted element
    printf("Print the new array with the inserted element:\n ");
    for (int i = 0; i < n; i++)
        printf("%d ", array1[i]);
```

output:
Enter a new number to insert into the first array:
8
Print the new array with the inserted element:
1 2 3 8


delete a special element:
```c
// Delete the second element from the first array
    for (int i = 1; i < n - 1; i++)
        array1[i] = array1[i + 1];

    n--; // Decrease the number of elements in the array

    // Print the first array without the second element
    printf("Print the array without the second element:\n ");
    for (int i = 0; i < n; i++)
        printf("%d ", array1[i]);
```

output:
1 3 8

sum and avg of elements :

```c
// Calculate the sum of elements in the first array
    int sum = 0;
    for (int i = 0; i < n; i++)
        sum += array1[i];

    // Calculate the average
    float average = (float)sum / n;

    // Print the sum and average
    printf("Sum of elements in the first array: %d\n", sum);
    printf("Average of elements in the first array: %.2f\n", average);
```
output:
Sum of elements in the first array: 12
Average of elements in the first array: 4.0

reverse:
```c
for (int i = 0, j = n - 1; i < j; i++, j--) {
        // Swap elements using a temporary variable
        int temp = array1[i];
        array1[i] = array1[j];
        array1[j] = temp;
    }

    // Print the reversed first array
    printf("Reversed array:");
    for (int i = 0; i < n; i++)
   printf("%d ", array1[i]);
```

output:
8 3 1

selection sort :
```c
 // Selection Sort
    for (int i = 0; i < n - 1; i++) {
        for (int j = i + 1; j < n; j++) {
            // Swap elements if element j is smaller than element i
            if (array1[j] < array1[i]) {
                // Swap operation
                int temp = array1[i];
                array1[i] = array1[j];
                array1[j] = temp;
            }
        }
    }

    // Print the sorted first array
    printf("\nSorted form of first array: ");
    for (int i = 0; i < n; i++)
        printf("%d ", array1[i]);
```

output:
Sorted form of first array:
1 3 8


find a target in array with linear serch:

```c
// Linear Search
 int target;

    // Target number for searching
    printf("Enter the target number: ");
    scanf("%d", &target);

    int i = 0;
    int result2 = -1;

    while (i < n) {
        // If the target is found
        if (array1[i] == target) {
            result2 = i;
            break;
        }

        i++;
    }

    if (result2 != -1)
        printf("%d found at index %d\n", target, result);
    else
        printf("%d not found.\n", target);
```
output;
Enter the target number:
8
8 found at index 2

max:
```c

    // Find the maximum number
    int maxNumber = 0;

    for (int i = 0; i < n; i++) {
        if (array1[i] > maxNumber)
            maxNumber = array1[i];
    }

    // Print the maximum number
    printf("Maximum number: %d\n", maxNumber);
```

output:
Maximum number: 
8

break an array:

```c
// Check if the number of elements is even for splitting
    if (n % 2 != 0) {
        printf("The number of array elements must be even to split from the middle.\n");
        printf("Enter a new number to insert into the first array:\n");
        scanf("%d", &newData);

        // Insert data into the first array
        array1[n] = newData;
        n++;

        // Print the first array with the inserted element
        printf("Print the new array with the inserted element:\n ");
        for (int i = 0; i < n; i++)
        printf("%d ", array1[i]);

        
    }

    // Calculate half of the number of elements
    int half = n / 2;

    // Create a second array for the first half
    int array_p2[half];
    for (int i = 0; i < half; i++)
        array_p2[i] = array1[i];

    // Create a third array for the second half
    int array3[half];
    for (int i = 0; i < half; i++)
        array3[i] = array1[half + i];

    // Print the first half
    printf("\nFirst half of the array: ");
    for (int i = 0; i < half; i++)
        printf("%d ", array_p2[i]);

    // Print the second half
    printf("\nSecond half of the array: ");
    for (int i = 0; i < half; i++)
        printf("%d ", array3[i]);
```

output:
The number of array elements must be even to split from the middle
Enter a new number to insert into the first array:
5
Print the new array with the inserted element:
1 3 8 5

First half of the array:
1 3
Second half of the array:
8 5

merge again:

```c
// Merge arrays again
    int mergedArray[n];

    for (int i = 0; i < half; i++) {
        mergedArray[i] = array2[i];
        mergedArray[half + i] = array3[i];
    }

    // Print the merged array
    printf("\nMerged array: ");
    for (int i = 0; i < n; i++)
        printf("%d ", mergedArray[i]);*/

```

output:
Merged array:
1 3 8 5

input a string and find world :
```c
  #define MAX_LENGTH 100

    char inputString[MAX_LENGTH];

    // Input a string
    printf("Enter a string: ");
    scanf("%[^\n]", inputString);

    // Define the special word to search for
    char specialWord[] = "raft";

    // Search for the special word in the string
    int i, j;
    for (i = 0; inputString[i] != '\0'; i++) {
        // If the current character matches the first character of the special word
        if (inputString[i] == specialWord[0]) {
            // Check if the subsequent characters match the special word
            for (j = 1; specialWord[j] != '\0' && inputString[i + j] == specialWord[j]; j++) {
                // Do nothing; continue checking characters
            }

            // If the loop reached the end of the special word, it means a match is found
            if (specialWord[j] == '\0') {
                printf("Special word '%s' found at index %d\n", specialWord, i);
                return 0; // Exit the program after finding the word
            }
        }
    }

    // If the loop completes without finding the special word
    printf("Special word '%s' not found.\n", specialWord);

    return 0;
}
```

output:
Enter a string:
ali raft be madrese!
Special word 'raft' found at index 3













