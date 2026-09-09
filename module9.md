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
#include <stdio.h>

#define MAX 100

int main()
{
    int stack[MAX], n, i;

    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        scanf("%d", &stack[i]);
    }

    printf("Stack elements are:\n");

    for (i = n - 1; i >= 0; i--)
    {
        printf("%d\n", stack[i]);
    }

    return 0;
}

Output:

<img width="205" height="61" alt="image" src="https://github.com/user-attachments/assets/e2ecec0a-b8e0-449c-bb7f-998600b7b255" />

<img width="242" height="155" alt="image" src="https://github.com/user-attachments/assets/99a35c92-9508-470b-be71-285963cf8673" />




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
#include <stdio.h>

#define MAX 100

int main()
{
    int stack[MAX], top = -1;
    int n, element;

    scanf("%d", &n);

    for (int i = 0; i < n; i++)
    {
        scanf("%d", &stack[++top]);
    }

    scanf("%d", &element);

    if (top == MAX - 1)
    {
        printf("Stack Overflow");
    }
    else
    {
        stack[++top] = element;

        printf("Stack after push:\n");
        for (int i = top; i >= 0; i--)
        {
            printf("%d\n", stack[i]);
        }
    }

    return 0;
}


Output:

<img width="213" height="141" alt="image" src="https://github.com/user-attachments/assets/6810c0dc-b455-4023-836d-fb253fa0d7b4" />





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
#include <stdio.h>

#define MAX 100

int main()
{
    int queue[MAX], n, i;

    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        scanf("%d", &queue[i]);
    }

    printf("Queue elements are:\n");

    for (i = 0; i < n; i++)
    {
        printf("%d ", queue[i]);
    }

    return 0;
}



Output:
<img width="228" height="57" alt="image" src="https://github.com/user-attachments/assets/07fa4b8e-31ca-481d-a675-9e3f52ea0d53" />



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
#include <stdio.h>

#define MAX 100

int main()
{
    int queue[MAX];
    int front = 0, rear = -1;
    int n, i, element;

    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        scanf("%d", &element);

        if (rear == MAX - 1)
        {
            printf("Queue Overflow");
            return 0;
        }

        queue[++rear] = element;
    }

    printf("Queue elements are:\n");

    for (i = front; i <= rear; i++)
    {
        printf("%d ", queue[i]);
    }

    return 0;
}

Output:
<img width="231" height="60" alt="image" src="https://github.com/user-attachments/assets/c6f617e8-0887-4cc8-add7-fbcea36a43ff" />


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
#include <stdio.h>

#define MAX 100

int queue[MAX];
int front = 0, rear = -1;

void delete()
{
    if (front > rear)
    {
        printf("Queue Underflow");
    }
    else
    {
        printf("Deleted element: %d\n", queue[front]);
        front++;
    }
}

int main()
{
    int n, i;

    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        scanf("%d", &queue[++rear]);
    }

    delete();

    printf("Queue after deletion:\n");

    for (i = front; i <= rear; i++)
    {
        printf("%d ", queue[i]);
    }

    return 0;
}

Output:
<img width="200" height="91" alt="image" src="https://github.com/user-attachments/assets/a8919d38-1357-48fa-a175-5950e696fea8" />



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
