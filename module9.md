EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

//type your code here
```
#include<stdio.h>
char stack[100];
int top;
void display()

{
    if(top==-1)
    {
        printf("stack is empty");
    }
    else
    {
       for(int i=top;i>=0;i--)
       {
           printf("%c\n",stack[i]);
       }
    }
}
```

Output:

//paste your output here
<img width="848" height="627" alt="image" src="https://github.com/user-attachments/assets/b0e14267-a38d-4a83-b417-0d4ae580046a" />



Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

//type your code here
```
char stack[100];
int size=3,top=-1;
void push (char data)
{
    if(top==size-1)
    {
        printf("stack is full\n");
    }
    else
    {
        stack[++top]=data;
    }
}
```

Output:
<img width="854" height="663" alt="image" src="https://github.com/user-attachments/assets/ea3821cb-9f5b-406b-9b74-efd8ed2c1896" />


//paste your output here




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

//type your code here
```
char queue[50];
int front ,rear,size;
void display()
{
    if(front==-1)
    {
        printf("No elements to display");
    }
    else
    {
        for(int i=front;i<=rear;i++)
        {
            printf("%c ",queue[i]);
        }
    }
}
```
Output:

//paste your output here

<img width="896" height="675" alt="image" src="https://github.com/user-attachments/assets/830f68c1-b3c7-4902-b874-4d6e4019c682" />

Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
#include<stdio.h>

#define SIZE 50
float queue[SIZE];
int front,rear;
void enqueue(float data)
{
    if (rear == SIZE - 1) {
        printf("Queue Overflow\n");
    } else {
        if (front == -1) front = 0;  // first insertion
        queue[++rear] = data;
    }
}
```
//type your code here

Output:

//paste your output here


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

//type your code here
```
int front, rear;
void dequeue()
{
    front++;
}
```

Output:

//paste your output here

<img width="846" height="773" alt="image" src="https://github.com/user-attachments/assets/5baa6d96-fb0a-4d38-b6dc-00c37b86c4c6" />

Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
