# Middle of Linked List:

## Approach 1(Regular Solution): 
- Traverse the whole linked list and count the no. of nodes. 
- Now traverse the list again till count/2 and return the node at count/2. 

### CODE: 

```c++
int getlength(Node* head){
  int len = 0;
  while(head != NULL){
    len++;
    head = head -> next;
  }
  
  return len;
}

Node *findMiddle(Node* head){
  int len = getlength(head);
  
  // Position of Middle Node
  int pos = (len/2)+1;
  
  //for returning middle node pointer
  Node *temp = head;
  int cnt =0;
  while(cnt<(ans-1)){
    temp = temp -> next;
    cnt++;
  }
  
  return temp;
}
```

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Approach 2(Optimized Solution):
- Traverse linked list using two-pointers. Move one pointer by one and the other pointers by two. 
- When the fast pointer reaches the end, the slow pointer will reach the middle of the linked list.

![middle-of-a-given-linked-list-in-C-and-Java1](https://github.com/IshaanAdarsh/TIL/assets/100434702/6b20a15e-e8e8-4250-a626-087fc4010162)

### CODE:

```c++
Node *findMiddle(Node* head){
  if(head == NULL || hea -> next == NULL)
    return head;
  
  //2 node - needed or not ?
  if(head -> next -> next == NULL){
    return head ->next;
  }
  
  Node* slow = head;
  Node* fast = head ->next;
  
  while(fast != NULL){
    fast = fast -> next;
    if(fast != NULL){
      fast = fast ->next;
    }
    
    slow = slow ->next;
  }
  
  return slow;
}
```

### OR (Smaller Code)

```c++
    ListNode* middleNode(ListNode* head) {
        ListNode *slow = head, *fast = head;
        while (fast && fast->next){
            slow = slow->next;
            fast = fast->next->next;
        }
        return slow;
    }
```

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)
