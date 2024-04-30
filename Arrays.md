# Arrays

## **What is an Array?**

An array is the simplest data structure where a collection of similar data elements takes place and each data element can be accessed directly by only using its index number.

## One-Dimensional Arrays

### **1. Declaration and then Initialization**

First, you declare an array by specifying the data type of its elements, followed by square brackets `[ ]` (which indicate it's an array), and then the array's name. After declaring, you can initialize it by allocating memory with the `new` keyword and specifying the size of the array.

```java
// Declaration
int[] myArray;
int myArray1[];
// Initialization
myArray = new int[5]; // Allocate memory for 5 integers
```

### **2. Declaration with Initialization**

You can declare an array and immediately initialize it with values. In this case, the size of the array is inferred from the number of values provided.

```java
// Declare and initialize an array with 5 elements
int[] myArray1 = new int[]{1, 2, 3, 4, 5};

int[] myArray = {1, 2, 3, 4, 5};
```
### **3. Using the `new` Keyword**

For more dynamic scenarios, where you might not know the values upfront but know the size of the array, you can use the **`new`** keyword to allocate memory for the array. You can then assign values to each element using their indices.

```java
// Declare and allocate memory for an array of 5 elements
int[] myArray = new int[5];

// Initialize elements
myArray[0] = 10;
myArray[1] = 20;
myArray[2] = 30;
myArray[3] = 40;
myArray[4] = 50;
```

## **How to print elements of an Array in Java?**

### **1. Using a For Loop**

You can iterate over the array using a traditional `for` loop and print each element individually.

```java
public class Main {
    public static void main(String[] args) {
        int[] numbers = {10, 20, 30, 40, 50};

        // Using a for loop to print elements
        System.out.println("Using for loop:");
        for (int i = 0; i < numbers.length; i++) {
            System.out.println("Element at index " + i + ": " + numbers[i]);
        }
    }
}
```
### **2. Using Enhanced For Loop (Foreach Loop)**

The enhanced for loop (foreach loop) allows for concise iteration over the elements of an array.

```java
public class Main {
    public static void main(String[] args) {
        int[] numbers = {10, 20, 30, 40, 50};

        // Using enhanced for loop to print elements
        System.out.println("Using enhanced for loop:");
        for (int number : numbers) {
            System.out.println(number);
        }
    }
}
```
### **3. Using `Arrays.toString()` Method**

If you want to print the entire array at once, you can use the **`Arrays.toString()`** method, which returns a string representation of the array contents.

```java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] numbers = {10, 20, 30, 40, 50};

        // Using Arrays.toString() method to print entire array
        System.out.println("Using Arrays.toString() method:");
        System.out.println(Arrays.toString(numbers));
    }
}
```

### Remove Even Integers from an Array

To remove even integers from an array in Java, you typically need to create a new array without the even elements. Since arrays in Java have a fixed size, you can't directly remove elements from them. Here's how you can achieve this:

```java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] originalArray = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

        // Count the number of odd elements in the array
        int oddCount = 0;
        for (int i = 0; i < originalArray.length; i++) {
            if (originalArray[i] % 2 != 0) {
                oddCount++;
            }
        }

        // Create a new array to hold only the odd elements
        int[] newArray = new int[oddCount];
        int newIndex = 0;
        for (int i = 0; i < originalArray.length; i++) {
            if (originalArray[i] % 2 != 0) {
                newArray[newIndex] = originalArray[i];
                newIndex++;
            }
        }

        // Print the new array
        System.out.println("Original Array: " + Arrays.toString(originalArray));
        System.out.println("Array with Even Integers Removed: " + Arrays.toString(newArray));
    }
}
```

## Reverse an Array

```java
public class ReverseArray {

  // Program to reverse an array
  public static void main(String[] args) {

    int[] array1 = {1, 2, 3, 4, 5};
    System.out.println("The original array is: ");

    for (int i = 0; i < array1.length; i++) {
      System.out.print(array1[i] + " ");
    }

    System.out.println();

    System.out.println("The reversed array is: ");
    //  for loop to iterate through the array in reverse order
    for (int i = array1.length - 1; i >= 0; i--) {
      System.out.print(array1[i] + " ");
    }
  }
}
```

### **Using a while loop to swap elements**

You can reverse an array in Java using a `while` loop by swapping the elements of the array from the beginning and end until you reach the middle. Here's a simple implementation:

```java
public class ReverseArray {
    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5};

        // Print original array
        System.out.println("Original Array:");
        printArray(array);

        // Reverse the array using while loop
        reverseArray(array);

        // Print reversed array
        System.out.println("\\nReversed Array:");
        printArray(array);
    }

    // Method to reverse the array using while loop
    public static void reverseArray(int[] array) {
        int start = 0;
        int end = array.length - 1;
				
        while (start < end) {
            // Swap elements at start and end indices
            int temp = array[start];
            array[start] = array[end];
            array[end] = temp;

            // Move to the next pair of elements
            start++;
            end--;
        }
    }

    // Method to print the elements of the array
    public static void printArray(int[] array) {
        for (int num : array) {
            System.out.print(num + " ");
        }
    }
}
```
This code defines a `reverseArray` method that takes an array as input and reverses it using a `while` loop. The loop swaps the elements at the beginning and end of the array until the `start` index is less than the `end` index. Finally, it prints the reversed array.
