# Linked List:
- Dynamic Data structure which is a collection of Nodes
### Advantages: 
  - Grow/Shrink at runtime
  - No Memory Wastage 
  - Easy Insterion and Delection (No shifting)

# Singly Linked List:
  - Node = DATA + NEXT NODE ADDRESS (Pointer of Node type)

![Singlelinkedlist](https://github.com/IshaanAdarsh/TIL/assets/100434702/f39c6e67-b980-43ae-8e75-d298637a2bb2)

```c++
class Node {

    public:
    int data;
    Node* next;

    //constructor
    Node(int data) {
        this -> data = data; //Data in the SLL
        this -> next = NULL; //Points to Null
    }

    //destructor
    ~Node() {
        int value = this -> data;
        //memory free
        if(this->next != NULL) {
            delete next;
            this->next = NULL;
        }
        cout << " memory is free for node with data " << value << endl;
    }

};
```
## Print the Linked List:

Print the LL by simple linear Traversal

```c++
void print(Node* &head) {
    if(head == NULL) {
        cout << "List is empty "<< endl;
        return ;
    }
    
    Node* temp = head;
    while(temp != NULL ) {
        cout << temp -> data << " ";
        temp = temp -> next;
    }
    cout << endl;
}
```

## InsertAtHead:

Adding a new node behine the ending node

![Linkedlist_insert_at_start](https://github.com/IshaanAdarsh/TIL/assets/100434702/afbfc64e-aec9-4d6c-a0ee-c2d63072d171)

```c++
// Given a reference (pointer to pointer) to the head of a list and an int, inserts a new node on the front of the list.
void InsertAtHead(Node** head_ref, int new_data)
{
	//allocate node
	Node* new_node = new Node();

	//put in the data
	new_node->data = new_data;

	//Make next of new node as head
	new_node->next = (*head_ref);

	//Move the head to point to the new node (first node )
	(*head_ref) = new_node;
}
```
-   **Time Complexity:** O(1)
-   **Auxiliary Space:** O(1)

## InsertAtTail:
Adding a new node ahead of the ending node

```c++
void insertAtTail(Node* &tail, int d) {
    //new node create
    Node* new_node = new Node(d);
    
    //make next of tail as new node
    tail -> next = new_node;
    
    //tail points to last node always
    tail  = new_node; // tail = tail -> next;
}
```
-   **Time Complexity:** O(1)
-   **Auxiliary Space:** O(1)

## InsertAtPosition:
Adding a new node at nth positon
- We need to insert node a (n-1) positon in tail fashion

![insertion-in-singly-linked-list-after-specified-node](https://github.com/IshaanAdarsh/TIL/assets/100434702/a50ff46c-c2da-4c8e-afe0-a81b448d2f39)

```c++
void insertAtPosition(Node* &tail, Node* & head, int position, int d) {

    //insert at Start
    if(position == 1) {
        insertAtHead(head, d);
        return;
    }
    
    Node* temp  = head;
    int cnt = 1;
    
    //Moves the pointer temp to (n-1)th position
    while(cnt < position-1) {
        temp = temp->next;
        cnt++;
    }

    //inserting at Last Position &to make tail point at end
    if(temp -> next == NULL) {
        insertAtTail(tail,d);
        return ;
    }

    //creating a node for d
    Node* nodeToInsert = new Node(d);

    //The address in nodeToInsert will point to original nth Position
    nodeToInsert -> next = temp -> next;
    
    //The (n-1)th position will point to temp
    temp -> next = nodeToInsert;
}
```
-   **Time Complexity:** O(N)
-   **Auxiliary Space:** O(1)

## Append (Add a node at the end):

![Linkedlist_insert_last](https://github.com/IshaanAdarsh/TIL/assets/100434702/8fdd16dc-5d69-4ff2-a0a0-42a145ff673e)

```c++
// Given a reference (pointer to pointer) to the head of a list and an int, appends a new node at the end
void append(Node** head_ref, int new_data)
{
	
	//allocate node
	Node* new_node = new Node();
	
	//Used in While loop
	Node *last = *head_ref;
	
	//Put in the data
	new_node->data = new_data;
	
	//This new node is going to be the last node, so make next of it as NULL
	new_node->next = NULL;
	
	//If the Linked List is empty,then make the new node as head
	if (*head_ref == NULL)
	{
		*head_ref = new_node;
		return;
	}
	
	//Else traverse till the last node
	while (last->next != NULL)
	{
		last = last->next;
	}
	
	//Change the next of last node
	last->next = new_node;
	return;
}
```
-   **Time complexity:** O(N)
    -   This method can also be optimized to work in O(1) by keeping an extra pointer to the tail of the linked list/
-   **Auxiliary Space:** O(1)

## DeleteNode:

Deleting a new node at nth positon

```c++
void deleteNode(int position, Node* & head) { 

    //deleting first or start node
    if(position == 1) {
        Node* temp = head;
        head = head -> next;
        //memory free start node
        temp -> next = NULL;  //Need to point the node to NULL for destructor call
        delete temp;
    }
    else
    {
        //deleting any middle node or last node
        Node* curr = head;
        Node* prev = NULL;

        int cnt = 1;
        while(cnt < position) {
            prev = curr;
            curr = curr -> next;
            cnt++;
        }

        prev -> next = curr -> next;
        curr -> next  = NULL; //Need to point the node to NULL for destructor call
        delete curr;

    }
}
```
-   **Time complexity:** O(N)
-   **Auxiliary Space:** O(1)
