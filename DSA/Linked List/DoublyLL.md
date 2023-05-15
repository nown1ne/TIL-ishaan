# Doubly Linked List:
- A doubly linked list (DLL) is a special type of linked list in which each node contains a pointer to the previous node as well as the next node of the linked list.
- NODE = PREV + DATA + NEXT

```c++
class Node {
    public:
    int data;
    Node* prev;
    Node* next;

    //constructor
    Node(int d ) {
        this-> data = d;
        this->prev = NULL;
        this->next = NULL;
    }

    ~Node() {
        int val = this -> data;
        if(next != NULL) {
            delete next;
            next = NULL;
        }
        cout << "memory free for node with data "<< val << endl;
    }
};
```

## Traversing and Printing the LL:

Function to Linear Traverse a LL and Printing the LL

```c++
//traversing a linked list
void print(Node* head) {
    Node* temp  = head ;

    while(temp != NULL) {
        cout << temp -> data << " ";
        temp  = temp -> next;
    }
    cout << endl;
}
```

## Length of a LL:

Function to give length of the Linked List

```c++
//gives length of Linked List
int getLength(Node* head) {
    int len = 0;
    Node* temp  = head ;

    while(temp != NULL) {
        len++;
        temp  = temp -> next;
    }

    return len;
}
```

## InsertAtHead (DLL):

Funtion to add a node at the front in a Doubly Linked List

![DLL_add_front1](https://github.com/IshaanAdarsh/TIL/assets/100434702/bd3f112c-a3f5-4ec4-995f-83db800cf3df)


```c++
// Given a reference (pointer to pointer) to the head
// of a list and an int, inserts a new node
// on the front of the list.
void InsertAtHead(Node** head_ref, int new_data)
{
	// 1. allocate node
	Node* new_node = new Node();

	// 2. put in the data
	new_node->data = new_data;

	// 3. Make next of new node as head and previous as NULL
	new_node->next = (*head_ref);
	new_node->prev = NULL;

	// 4. change prev of head node to new node
	if ((*head_ref) != NULL)
		(*head_ref)->prev = new_node;

	// 5. move the head to point to the new node
	(*head_ref) = new_node;
}
```

## InsertAtTail (DLL):

Function to add a node at the tail in a Doubly Linked List

```c++
void insertAtTail(Node* &tail,Node* &head, int d) {
    if(tail == NULL) {
        Node* temp = new Node(d);
        tail = temp;
        head = temp;
    }
    else{
        Node* temp = new Node(d);
        tail -> next  = temp;
        temp -> prev = tail;
        tail = temp;
    }
}
```

## Add a node at the end in a Doubly Linked List:

![DLL_add_end1](https://github.com/IshaanAdarsh/TIL/assets/100434702/d3701030-64e9-4e09-93f7-50a7e3bbbf33)

```c++
// Given a reference (pointer to pointer) to the head
// of a DLL and an int, appends a new node at the end
void append(Node** head_ref, int new_data)
{
	// 1. allocate node
	Node* new_node = new Node();

	Node* last = *head_ref; /* used in step 5*/

	// 2. put in the data
	new_node->data = new_data;

	// 3. This new node is going to be the last node, so
	// make next of it as NULL
	new_node->next = NULL;

	// 4. If the Linked List is empty, then make the new
	// node as head
	if (*head_ref == NULL) {
		new_node->prev = NULL;
		*head_ref = new_node;
		return;
	}

	// 5. Else traverse till the last node
	while (last->next != NULL)
		last = last->next;

	// 6. Change the next of last node
	last->next = new_node;

	// 7. Make last node as previous of new node
	new_node->prev = last;

	return;
}
```

## InsertAtPosition:

Function to add a node at the any nth position in a Doubly Linked List

![DLL_add_middle1](https://github.com/IshaanAdarsh/TIL/assets/100434702/ff5d32b6-da79-46f8-9c69-6e6c46ec2e69)

```c++
void insertAtPosition(Node* & tail, Node* &head, int position, int d) {
    
    //insert at Start
    if(position == 1) {
        insertAtHead(tail,head, d);
        return;
    }

    Node* temp  = head;
    int cnt = 1;

    while(cnt < position-1) {
        temp = temp->next;
        cnt++;
    }

    //inserting at Last Position
    if(temp -> next == NULL) {
        insertAtTail(tail,head,d);
        return ;
    }

    //creating a node for d
    Node* nodeToInsert = new Node(d);

    nodeToInsert ->next = temp -> next;
    temp -> next -> prev = nodeToInsert;
    temp -> next = nodeToInsert;
    nodeToInsert -> prev = temp;
}
```

## Delete a Node:

![ezgif com-gif-maker1](https://github.com/IshaanAdarsh/TIL/assets/100434702/84ede179-a965-4da7-ac6f-9ee08908943d)

```c++
void deleteNode(int position, Node* & head) { 

    //deleting first or start node
    if(position == 1) {
        Node* temp = head;
        temp -> next -> prev = NULL;
        head = temp ->next;
        temp -> next = NULL;
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

        curr -> prev = NULL;
        prev -> next = curr -> next;
        curr -> next = NULL;

        delete curr;

    }
}
```
