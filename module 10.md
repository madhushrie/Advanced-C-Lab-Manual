EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

//type your code here
```
struct Node{
    char data; 
    struct Node *next;
}*head;

void search(char value)
{
    struct Node* temp=head;
    int pos=1;
    while(temp!=0){
        if(temp->data==value){
            printf("item %c found at location %d\n",value,pos);
            return;
        }
        
        temp=temp->next;
        pos++;
        
        
    }
    printf("Item not found");
 
 
 
 
 
}
```

Output:

//paste your output here

<img width="1151" height="544" alt="image" src="https://github.com/user-attachments/assets/2028da70-cbe6-41ab-95c5-82f784651280" />


Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

//type your code here
```
struct Node{
    int data; 
    struct Node *next;
}*head;


void insert(int data)
{
    struct Node* n=(struct Node*)malloc(sizeof(struct Node));
    if(head==NULL){
        head=n;
        n->data=data;
        n->next=NULL;
        return;
    }
    struct Node* temp=head;
    while(temp->next!=NULL){
        temp=temp->next;
        
    }
    n->data=data;
    n->next=NULL;
    temp->next=n;
    
}
```

Output:

//paste your output here
<img width="672" height="545" alt="image" src="https://github.com/user-attachments/assets/7580ef6a-60b8-49b5-8cfe-c0bd00ebdc02" />

 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

//type your code here
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void display()
{
    
    struct Node* temp=head;
    if(head==NULL){
        printf("List is empty\n");
        return;
    }
    while(temp!=NULL){
        printf("%.2f \n",temp->data);
        temp=temp->next;
    }
    
    
}
```

Output:

//paste your output here
<img width="650" height="518" alt="image" src="https://github.com/user-attachments/assets/bc82afc3-329b-401d-9c17-c91328418024" />



Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head;

void insert(int value)
{
    struct Node *newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->prev = NULL;
    newNode->next = NULL;

    if (head == NULL) {
        head = newNode;
    } else {
        struct Node *temp = head;
        while (temp->next != NULL) {
            temp = temp->next;
        }
        temp->next = newNode;
        newNode->prev = temp;
    }
    
    
    
}
```

//type your code here

Output:

//paste your output here
<img width="676" height="497" alt="image" src="https://github.com/user-attachments/assets/7b06c892-f0c9-4463-b78a-71ceae994595" />



Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
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


Program:

//type your code here
```
struct Node
{
    int data; 
    struct Node *next;
}*head;
void delete()
{
    struct Node* ptr=head;
    if(ptr== NULL)
    {
        printf("List is empty\n");
    }
    else
    {
        ptr = head;
        head = ptr->next;
        free(ptr);
        printf("Node deleted from the begining ...\n");
        
    }
}
```

Output:

//paste your output here

<img width="1070" height="685" alt="image" src="https://github.com/user-attachments/assets/f9711777-0dde-4813-9d30-19b24019b7df" />




Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





