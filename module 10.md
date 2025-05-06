## EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
### Aim:
To write a C program to search a given element in the given linked list.

### Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
### Program:
```
struct Node{
    float data; 
    struct Node *next;
}*head;
void search(float data)
{
    struct Node *ptr;
    char item=data;
    int i=0,flag;
    ptr = head;
    if(ptr == NULL)
    {
    printf("\nEmpty List\n");
    }
    else
    {
        while (ptr!=NULL)
        {
            if(ptr->data == item)
            {
                printf("item %c found at location %d ",item,i+1);
                flag=0;
            }
            i++;
            ptr = ptr -> next;
        }
        if(flag!=0)
        {
            printf("Item not found\n");
        }
    }
}
```
### Output:
![image](https://github.com/user-attachments/assets/4ad74c71-f9db-4278-8e81-7eaf4ffb39f6)

### Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
## EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
### Aim:
To write a C program to insert a node in a linked list.
### Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
### Program:
```
struct Node{
    char data; 
    struct Node *next;
}*head;
void insert(int data)
{
    struct Node *p=(struct Node*)malloc(sizeof(struct Node*));
    p->data=data;
    if(head==NULL){
        head=p;
        head->next=NULL;
    }
    else{
        struct Node *t=head;
        if(t->next!=NULL){
            t=t->next;
        }
        t->next=p;
    }
}
```
### Output:
![image](https://github.com/user-attachments/assets/1f7f76a0-f734-4200-8bbf-010c83f1e6c1)

### Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
## EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
### Aim:
To write a C program to traverse a doubly linked list.

### Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
### Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head,*temp;

void display()
{
    temp=head;
    while(temp!=NULL){
        printf("%d ",temp->data);
        temp=temp->next;
    }
}
```
### Output:
![image](https://github.com/user-attachments/assets/79629659-f0bd-4699-8be4-7d56c216199a)

### Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



## EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
### Aim:
To write a C program to insert an element in doubly linked list

### Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
### Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    char data;
}*head,*tail;

void insert(char data)
{
   struct Node *n=(struct Node *)malloc(sizeof(struct Node));
   n->data=data;
   n->prev=0;
   n->next=0;
    if(head==NULL){
        head=n;
        tail=n;
    }
    else{
        tail->next=n;
        n->prev=tail;
        tail=n;
    }
}
```
### Output:
![image](https://github.com/user-attachments/assets/9ab3775f-70e4-43e0-9766-fbb63471ed96)

### Result:
Thus, the program to insert an element in doubly linked list is verified successfully.

## EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

### Aim:
To write a C function that deletes a given element from a linked list.

### Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


### Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    char data;
}*head,*temp;

void delete()
{
    if(head==NULL){
        printf("UNDERFLOW\n");
    }
    else if(head->next==NULL){
        head=NULL;
        free(head);
        printf("Node deleted\n");
    }
    else{
        temp=head;
        head=temp->next;
        head->prev=NULL;
        free(temp);
        printf("Node deleted\n");
    }
}
```
### Output:
![image](https://github.com/user-attachments/assets/23f86a27-8cba-4985-846f-1d875c470ea5)

### Result:
Thus, the function that deletes a given element from a linked list is verified successfully.
