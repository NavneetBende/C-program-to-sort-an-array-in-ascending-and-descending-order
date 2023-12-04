# C-program-to-sort-an-array-in-ascending-and-descending-order

Sort the array in C
Here, on this page, we will discuss the program to sort the array in the C programming language. We are given an array and need to sort it in ascending and descending order. Methods for sorting of array in C, We will discuss various algorithms to sort the given input array.

Sort the array in C
Different methods Discussed in this page are :
Method 1 : Using Selection Sort
Method 2 : Using Insertion Sort
Method 3 : Using Bubble Sort
 
Method 1 :
In this method we will use Selection Sorting Technique to sort the given input array. You can click on the button given below to understand the algorithm for selection sorting technique.

Sort the array in C
Algorithm For Selection Sort
Method 1 : Code in C
Run
// C program for implementation of selection sort 
#include <stdio.h>

void swap(int *xp, int *yp) 
{ 
   int temp = *xp; 
   *xp = *yp; 
   *yp = temp; 
}

void selectionSort(int array[], int size) 
{ 
    int i, j, min_idx;

    // Loop to iterate on array 
    for (i = 0; i < size-1; i++) 
    { 
        // Here we try to find the min element in array 
        min_idx = i; 
        for (j = i+1; j < size; j++)
        {
            if (array[j] < array[min_idx]) 
              min_idx = j; 
        }
        // Here we interchange the min element with first one 
        swap(&array[min_idx], &array[i]); 
     } 
}

/* Display function to print values */
void display(int array[], int size) 
{ 
    int i; 
    for (i=0; i < size; i++)
    { 
       printf("%d ",array[i]);
    }
     printf("\n"); 
}

// The main function to drive other functions 
int main() 
{ 
   int array[] = {50, 30, 10, 90, 80, 20, 40, 70}; 
   int size = sizeof(array)/sizeof(array[0]);

   selectionSort(array, size);
  
   display(array, size);

   return 0; 
}
Output
10 20 30 40 50 70 80 90
Related Pages
Reverse an Array

Sort first half in ascending order and second half in descending

Finding the frequency of elements in an array

Sorting elements of an array by frequency

Finding the Longest Palindrome in an Array

Method 2 :
In this method we will use Insertion Sorting Technique to sort the given input array. You can click on the button given below to understand the algorithm for insertion sorting technique.

Algorithm For Insertion Sort
Method 2 : Code in C
Run
#include<stdio.h> 

// Here we are implementing Insertion sort
void insertionSort(int array[], int size) 
{ 
   int i, target, j; 
   for (i = 1; i < size; i++) { target = array[i]; j = i - 1; /* Here the elements in b/w arrary[0 to i-1] which are greater than target are moved ahead by 1 position each*/ while (j >= 0 && array[j] > target) 
       { 
           array[j + 1] = array[j]; 
           j = j - 1; 
       } 
       array[j + 1] = target; 
   }
}

/* Function to print array */
void display(int arr[], int size) 
{ 
    int i; 
    for (i=0; i < size; i++) 
      printf("%d ", arr[i]); 
    printf("\n"); 
}

// Main function to run the program
int main() 
{ 
   int array[] = {50, 30, 10, 90, 80, 20, 40, 70}; 
   int size = sizeof(array)/sizeof(array[0]);

   insertionSort(array, size);

   display(array, size); 
   return 0; 
}
Output
10 20 30 40 50 60 70 80 90
Method 3 :
In this method we will use Bubble Sorting Technique to sort the given input array. You can click on the button given below to understand the algorithm for bubble sorting technique.

Algorithm For Bubble Sort
Method 3 : Code in C
Run
#include<stdio.h> 

void swap(int *var1, int *var2) 
{ 
   int temp = *var1; 
   *var1 = *var2; 
   *var2 = temp; 
}

// Here we are implementing bubbleSort
void bubbleSort(int arr[], int n) 
{ 
   int i, j; 
   for (i = 0; i < n-1; i++){

        // Since, after each iteration righmost i elements are sorted 
        for (j = 0; j < n-i-1; j++) if (arr[j] > arr[j+1]) 
              swap(&arr[j], &arr[j+1]); 
    }
}

/* Function to print array */
void display(int arr[], int size) 
{ 
   int i; 
   for (i=0; i < size; i++) 
      printf("%d ", arr[i]); 
   printf("\n"); 
}

// Main function to run the program
int main() 
{ 
    int array[] = {50, 30, 10, 90, 80, 20, 40, 70}; 
    int size = sizeof(array)/sizeof(array[0]);

    bubbleSort(array, size);

    display(array, size); 
    return 0; 
}
Output
10 20 30 40 50 60 70 80 90
