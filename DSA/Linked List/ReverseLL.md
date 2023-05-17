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

## Approach 2 (Recursive Solution):
Follow the steps below to solve the problem:

-   Divide the list in two parts -- first node and rest of the linked list.
-   Call reverse for the rest of the linked list.
-   Link the rest linked list to first.
-   Fix head pointer to NULL

![Linked-List-Rverse](https://github.com/IshaanAdarsh/TIL/assets/100434702/cc6e605b-6aff-4641-b91f-17d6d149432f)

```c++

```

- **Time Complexity:** O(N)
- **Space Complexity:** O(N)
