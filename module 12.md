

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
```
struct Node   
{  
int data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *ptr;
    ptr=head;
    while(ptr!=NULL)
    {
        printf("%d \n",ptr->data);
        ptr=ptr->next;
    }
}
```
Output:
![image](https://github.com/user-attachments/assets/7d072e85-f46f-40bd-85e9-47e622d71e3e)

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
```
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void pop()  
{  
    struct Node *ptr;  
    if(head==NULL)  
    {  
        printf("stack is empty");  
    }  
    else  
    {  
        ptr=head;  
        head=ptr->next;  
        free(ptr);  
    }  
}  
```
Output:
![image](https://github.com/user-attachments/assets/9060a9fe-c6d1-43b0-b313-fc99af4d0458)

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
```
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    struct Node *temp=front;   
    if(front!=0)
    {
        printf("queue elements: \n");
        while(temp!=0)
        {
            printf("%c \n",temp->data);
            temp=temp->next;
        }
    }
    else
    {
        printf("queue is empty");
    }
}
```
Output:
![image](https://github.com/user-attachments/assets/72bbd78e-c686-45ce-bfbd-5434fbd86de0)

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
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(float data)
{
    struct Node *ptr=(struct Node*)malloc(sizeof(struct Node));
    ptr->data=data;
    ptr->next=NULL;
    if(front==0)
    {
        front=rear=ptr;
    }
    else
    {
        rear->next=ptr;
        rear=ptr;
    }
}
```
Output:
![image](https://github.com/user-attachments/assets/6bd3aa57-bc1f-4fa5-b9e1-c29bf75cedd0)

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
```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%d \n",front->data);
}
```
Output:
![image](https://github.com/user-attachments/assets/6bb2b736-df75-4709-98ec-9d77400f9cec)

Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


