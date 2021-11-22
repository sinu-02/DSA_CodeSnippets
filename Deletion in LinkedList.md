# Case 1: Deleting the first element from the linked list


struct Node * deleteFirst(struct Node * head)
{
    struct Node * ptr = head;
    head = head->next;
    free(ptr);
    return head;
}

# Case 2: Deleting the element at a given index from the linked list


struct Node * deleteAtIndex(struct Node * head, int index)
{
    struct Node *p = head;
    struct Node *q = head->next;
    for (int i = 0; i < index-1; i++)
    {
        p = p->next;
        q = q->next;
    }
    
    p->next = q->next;
    free(q);
    return head;
}

# Case 3: Deleting the last element

struct Node * deleteAtLast(struct Node * head)
{
    struct Node *p = head;
    struct Node *q = head->next;
    while(q->next !=NULL)
    {
        p = p->next;
        q = q->next;
    }
    
    p->next = NULL;
    free(q);
    return head;
}

# Case 4: Deleting the element with a given value from the linked list

struct Node * deleteByValue(struct Node * head, int value)
{
    struct Node *p = head;
    struct Node *q = head->next;
    while(q->data!=value && q->next!= NULL)
    {
        p = p->next;
        q = q->next;
    }
    
    if(q->data == value){
        p->next = q->next;
        free(q);
    }
    return head;
}

