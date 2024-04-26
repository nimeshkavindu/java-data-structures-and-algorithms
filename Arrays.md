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


