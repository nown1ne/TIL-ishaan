# Reverse Linked List:
## Appraoch 1 (Iterative Method):

-   Initialize three pointers **prev** as NULL, **curr** as **head**, and **next** as NULL.
-   Iterate through the linked list. In a loop, do the following:
    -   Before changing the **next** of **curr**, store the **next** node 
        -   next = curr -> next
    -   Now update the **next** pointer of **curr** to the **prev** 
        -   curr -> next = prev 
    -   Update **prev** as **curr** and **curr** as **next** 
        -   prev = curr 
        -   curr = next

![RGIF2](https://github.com/IshaanAdarsh/TIL/assets/100434702/625def69-85cc-4d02-84b3-f00edf9e4d18)

### CODE:
```c++
Node* reverseLinkedList(Node *head)
{
  if(head == NULL || head -> next == NULL){
    return head;
  }
  
  // Initialize current, previous and next pointers
  Node* prev = NULL;
  Node* curr = head;
  Node* forward = NULL:
  
  while(curr != NULL){
    // Store forward
    forward = curr -> next;
    //Reverse current node's pointer
    curr -> next = prev;
    //Move pointers one position ahead
    prev = curr;
    curr = forward;
  }
  
  return prev;
}
```

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Approach 2 (Tail Recursive Method):
Follow the steps below to solve the problem:

-   First update next with next node of current i.e. **next = current->next**
-   Now make a reverse link from current node to previous node i.e. curr->next = prev
-   If the visited node is the last node then just make a reverse link from the current node to previous node and update head.

```c++
viod reverse(Node* &head, Node* curr, Node* prev)
{
    //base case
    if(curr==NULL){
        //point head to prev and return
        head = prev;
        return;
    }
    
    //Move the pointer forward
    Node* forward = curr -> next;
    
    //call the function recursively
    reverse(head,forward,curr);
    
    //Solves the current case (reverses the LL)
    curr -> next = prev;
}

Node*reverseLinkedList(Node *head)
{
    Node* curr = head;
    Node* prev = NULL;
    reverse(head,curr,prev);
    return head;
}
```

- **Time Complexity:** O(N)
- **Space Complexity:** O(N)

## Approach 3 (Recursive Method):

Follow the steps below to solve the problem:

-   Divide the list in two parts -- first node and rest of the linked list.
-   Call reverse for the rest of the linked list.
-   Link the rest linked list to first.
-   Fix head pointer to NULL

![Linked-List-Rverse](https://github.com/IshaanAdarsh/TIL/assets/100434702/cc6e605b-6aff-4641-b91f-17d6d149432f)

```c++
Node* reverse(Node* head)
    {
        if (head == NULL || head->next == NULL)
            return head;
 
        //reverse the rest list and put the first element at the end
        Node* rest = reverse(head->next);
        head->next->next = head;
 
        //tricky step -- see the diagram
        head->next = NULL;
 
        // fix the head pointer 
        return rest;
    }
```

- **Time Complexity:** O(N)
- **Space Complexity:** O(N)
