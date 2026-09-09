EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

int main()
{
    struct Node *top = NULL;
    struct Node *newNode;
    int n, i;

    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        newNode = (struct Node *)malloc(sizeof(struct Node));

        scanf("%d", &newNode->data);

        newNode->next = top;
        top = newNode;
    }

    printf("Stack elements are:\n");

    while (top != NULL)
    {
        printf("%d\n", top->data);
        top = top->next;
    }

    return 0;
}

Output:
<img width="178" height="55" alt="image" src="https://github.com/user-attachments/assets/4f940353-a9d0-4f93-aff3-72b7c6df8e63" />
<img width="200" height="156" alt="image" src="https://github.com/user-attachments/assets/190889e7-c2b2-41bc-b4f3-cd9eabb101a6" />




Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

int main()
{
    struct Node *top = NULL;
    struct Node *newNode;
    int n, i;

    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        newNode = (struct Node *)malloc(sizeof(struct Node));

        scanf("%d", &newNode->data);

        newNode->next = top;
        top = newNode;
    }

    if (top == NULL)
    {
        printf("Stack Underflow");
    }
    else
    {
        printf("Popped element: %d", top->data);

        newNode = top;
        top = top->next;
        free(newNode);
    }

    return 0;
}
Output:
<img width="162" height="60" alt="image" src="https://github.com/user-attachments/assets/4d6c022f-356b-4672-9dd6-228fb75c2d8b" />
<img width="191" height="35" alt="image" src="https://github.com/user-attachments/assets/f151ce63-567b-4123-a2e8-666a0824aa58" />

Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

int main()
{
    struct Node *front = NULL;
    struct Node *rear = NULL;
    struct Node *newNode;
    struct Node *temp;
    int n, i;

    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        newNode = (struct Node *)malloc(sizeof(struct Node));

        scanf("%d", &newNode->data);
        newNode->next = NULL;

        if (front == NULL)
        {
            front = newNode;
            rear = newNode;
        }
        else
        {
            rear->next = newNode;
            rear = newNode;
        }
    }

    printf("Queue elements are:\n");

    temp = front;

    while (temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }

    return 0;
}

Output:
<img width="176" height="53" alt="image" src="https://github.com/user-attachments/assets/6166d57d-bf41-44ab-bb8e-31de538fce3f" />
<img width="196" height="58" alt="image" src="https://github.com/user-attachments/assets/2d03b611-0950-4e42-854b-7720727fbb29" />


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

int main()
{
    struct Node *front = NULL;
    struct Node *rear = NULL;
    struct Node *newNode;
    struct Node *temp;
    int n, i;

    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        newNode = (struct Node *)malloc(sizeof(struct Node));

        scanf("%d", &newNode->data);
        newNode->next = NULL;

        if (front == NULL)
        {
            front = newNode;
            rear = newNode;
        }
        else
        {
            rear->next = newNode;
            rear = newNode;
        }
    }

    printf("Queue elements are:\n");

    temp = front;

    while (temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }

    return 0;
}

Output:
<img width="122" height="50" alt="image" src="https://github.com/user-attachments/assets/20fb4b5c-1cf2-4e26-b50f-86846ac5fccb" />
<img width="190" height="62" alt="image" src="https://github.com/user-attachments/assets/a07fe595-c312-4132-ac20-d4c484390e0d" />


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

int main()
{
    struct Node *front = NULL;
    struct Node *rear = NULL;
    struct Node *newNode;
    int n, i;

    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        newNode = (struct Node *)malloc(sizeof(struct Node));

        scanf("%d", &newNode->data);
        newNode->next = NULL;

        if (front == NULL)
        {
            front = newNode;
            rear = newNode;
        }
        else
        {
            rear->next = newNode;
            rear = newNode;
        }
    }

    if (front == NULL)
    {
        printf("Queue is empty");
    }
    else
    {
        printf("Peek element: %d", front->data);
    }

    return 0;
}


Output:
<img width="157" height="55" alt="image" src="https://github.com/user-attachments/assets/263c1bfd-7043-4cea-8550-595b2ed45f8d" />
<img width="206" height="31" alt="image" src="https://github.com/user-attachments/assets/de66f35e-de28-4f13-bbc4-3c6dd5a4af68" />





Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.
