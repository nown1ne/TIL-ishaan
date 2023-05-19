# Circular Linked List:

There are 2 types of Linked List:
- **Circular Singly Linked List:**
  -  Singly linked list, the last node of the list contains a pointer to the first node of the list.
  -  We use only tail in circular LL 
    - As tail -> next = Head

![CircularSinglyLinkedList-660x172](https://github.com/IshaanAdarsh/TIL/assets/100434702/730091e8-3574-4eda-bf07-f5d1cf20dd65)


- **Circular Doubly Linked List:**
  - Circular Doubly Linked List has properties of both doubly linked list and circular linked list in which two consecutive elements are linked or connected by the previous and next pointer and the last node points to the first node by the next pointer and also the first node points to the last node by the previous pointer.

![Circulardoublylinkedlist-660x155](https://github.com/IshaanAdarsh/TIL/assets/100434702/62bbcbaf-5e74-4489-aac6-bced6189c53f)

```c++
class Node {
    public:
    int data;
    Node* next;

    //constrcutor
    Node(int d) {
        this->data = d;
        this->next = NULL;
    }

    ~Node() {
        int value = this->data;
        if(this->next != NULL) {
            delete next;
            next = NULL;
        }
        cout << " memory is free for node with data " << value << endl;
    }

};
```

## InsetAtTail:

```c++
void insertNode(Node* &tail, int element, int d) {
    
    //empty list
    if(tail == NULL) {
        Node* newNode = new Node(d);
        tail = newNode;
        newNode -> next = newNode;
    }
    else{
        //non-empty list
        //assuming that the element is present in the list

        Node* curr = tail;

        while(curr->data != element) {
            curr = curr -> next;
        }
        
        //element found -> curr is representing element wala node
        Node* temp = new Node(d);
        temp -> next = curr -> next;
        curr -> next = temp;

    }

}    
```
## Print and Traversal of a Circular LL:

```c++
void print(Node* tail) {

    Node* temp = tail;

    //empty list
    if(tail == NULL) {
        cout << "List is Empty "<< endl;
        return ;
    }

    do {
        cout << tail -> data << " ";
        tail = tail -> next;
    } while(tail != temp);

    cout << endl;
} 
```

## Delete Node:

```c++
void deleteNode(Node* &tail, int value) {

    //empty list
    if(tail == NULL) {
        cout << " List is empty, please check again" << endl;
        return;
    }
    else{
        //non-empty

        //assuming that "value" is present in the Linked List
        Node* prev = tail;
        Node* curr = prev -> next;

        while(curr -> data != value) {
            prev = curr;
            curr = curr -> next;
        }

        prev -> next = curr -> next;

        //1 Node Linked List
        if(curr == prev) {
            tail = NULL;
        }

        //>=2 Node linked list
        else if(tail == curr ) {
            tail = prev;
        }

        curr -> next = NULL;
        delete curr;
    }
}
```

## ifCircular:
**Problem** : Checks of the linked list is circular LL or not.

### Approach 1:

-   Declare a Node pointer node and initialize it to the head's next
-   Move node pointer to the next node, while the node is not equal to nullptr and node is not equal to the head
-   After coming out of the loop, check if the node is equal to head then return true, else return false

### CODE:

```c++
bool isCircularList(Node* head) {

    //empty list
    if(head == NULL) {
        return true;
    }

    Node* temp = head -> next;
    while(temp != NULL && temp != head ) {
        temp = temp -> next;
    }

    if(temp == head ) {
        return true;
    }

    return false;

}
```

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

### Approach 2 (Using Map) {Shite way}

- **Time Complexity:** O(N)
- **Space Complexity:** O(N)
