# EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
## Aim:
To write a C program to display stack elements using linked list.

## Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
## Program:
```
#include <stdio.h>

// Function to find the greatest among four numbers
int max_of_four(int n1, int n2, int n3, int n4) {
    int max = n1;

    if (n2 > max) {
        max = n2;
    }
    if (n3 > max) {
        max = n3;
    }
    if (n4 > max) {
        max = n4;
    }

    return max;
}

int main() {
    int n1, n2, n3, n4, greater;

    printf("Enter four integers: ");
    scanf("%d %d %d %d", &n1, &n2, &n3, &n4);

    greater = max_of_four(n1, n2, n3, n4);

    printf("The greatest number is: %d\n", greater);

    return 0;
}
```

## Output:
```
Enter four integers: 12 45 7 30
The greatest number is: 45
```


## Result:
Thus, the program to display stack elements using linked list is verified successfully. 



# EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
## Aim:
To write a C program to pop an element from the given stack using liked list.

## Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
## Program:
```
#include <stdio.h>

void calculate_the_max(int n, int k) {
    int max_and = 0, max_or = 0, max_xor = 0;

    // Iterate over all pairs (i, j) where 1 <= i < j <= n
    for (int i = 1; i <= n; i++) {
        for (int j = i + 1; j <= n; j++) {
            int and_val = i & j;
            int or_val = i | j;
            int xor_val = i ^ j;

            // Update max AND value less than k
            if (and_val > max_and && and_val < k)
                max_and = and_val;

            // Update max OR value less than k
            if (or_val > max_or && or_val < k)
                max_or = or_val;

            // Update max XOR value less than k
            if (xor_val > max_xor && xor_val < k)
                max_xor = xor_val;
        }
    }

    printf("Maximum AND value less than %d is: %d\n", k, max_and);
    printf("Maximum OR value less than %d is: %d\n", k, max_or);
    printf("Maximum XOR value less than %d is: %d\n", k, max_xor);
}

int main() {
    int n, k;

    printf("Enter two integers (n and k): ");
    scanf("%d %d", &n, &k);

    calculate_the_max(n, k);

    return 0;
}
```

## Output:

```
Enter two integers (n and k): 5 4
Maximum AND value less than 4 is: 2
Maximum OR value less than 4 is: 3
Maximum XOR value less than 4 is: 3
```


## Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
# EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
## Aim:
To write a C program to display queue elements using linked list.
## Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
## Program:

```
#include <stdio.h>

int main() {
    int noshel, noque;
    printf("Enter number of shelves and queries: ");
    scanf("%d %d", &noshel, &noque);

    int shelarr[noshel][1000]; // Assuming max 1000 books per shelf
    int nobookarr[noshel];     // To store number of books in each shelf

    // Initialize number of books on each shelf to 0
    for (int i = 0; i < noshel; i++) {
        nobookarr[i] = 0;
    }

    int k, c;
    for (int q = 0; q < noque; q++) {
        int queryType;
        printf("Enter query type: ");
        scanf("%d", &queryType);

        if (queryType == 1) {
            // Query 1: Add a book with pages 'c' to shelf 'k'
            printf("Enter shelf index and book pages: ");
            scanf("%d %d", &k, &c);
            shelarr[k][nobookarr[k]] = c;
            nobookarr[k]++;
        }
        else if (queryType == 2) {
            // Query 2: Print pages of the 'c'-th book on shelf 'k'
            printf("Enter shelf index and book index: ");
            scanf("%d %d", &k, &c);
            if (c < nobookarr[k])
                printf("Pages: %d\n", shelarr[k][c]);
            else
                printf("Invalid book index\n");
        }
        else if (queryType == 3) {
            // Query 3: Print number of books on shelf 'k'
            printf("Enter shelf index: ");
            scanf("%d", &k);
            printf("Number of books: %d\n", nobookarr[k]);
        }
        else {
            printf("Invalid query type\n");
        }
    }

    return 0;
}
```

## Output:
```
Enter number of shelves and queries: 2 5
Enter query type: 1
Enter shelf index and book pages: 0 100
Enter query type: 1
Enter shelf index and book pages: 1 200
Enter query type: 2
Enter shelf index and book index: 0 0
Pages: 100
Enter query type: 3
Enter shelf index: 1
Number of books: 1
Enter query type: 2
Enter shelf index and book index: 1 0
Pages: 200
```

## Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
# EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

## Aim:
To write a C program to insert elements in queue using linked list

## Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
## Program:

```
#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter the number of integers: ");
    scanf("%d", &n);

    int a[n];  // Array to store integers

    printf("Enter %d integers:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &a[i]);
        sum += a[i];
    }

    printf("Sum of the integers is: %d\n", sum);

    return 0;
}
```
## Output:

```
Enter the number of integers: 5
Enter 5 integers:
10 20 30 40 50
Sum of the integers is: 150
```

## Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



# EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


## Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

## Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

## Program:
```

#include <stdio.h>
#include <ctype.h>

int main() {
    char sentence[1000];
    int i = 0, wordCount = 0;
    int inWord = 0;  // Flag to track if we are inside a word

    printf("Enter a sentence:\n");
    fgets(sentence, sizeof(sentence), stdin);

    while (sentence[i] != '\0') {
        if (isspace(sentence[i]) || ispunct(sentence[i])) {
            // If space or punctuation, we are not inside a word
            inWord = 0;
        } else if (inWord == 0) {
            // Start of a new word
            inWord = 1;
            wordCount++;
        }
        i++;
    }

    printf("Number of words: %d\n", wordCount);

    return 0;
}
```

## Output:

```

Enter a sentence:
Hello, how are you doing today?
Number of words: 6
```



## Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


