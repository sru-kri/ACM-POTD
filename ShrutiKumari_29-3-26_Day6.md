/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 */
struct ListNode* reverseList(struct ListNode* head) {
    struct ListNode* prev = NULL;  
    struct ListNode* curr = head;  
    struct ListNode* next = NULL;  

    while (curr != NULL) {
        next = curr->next;   
        curr->next = prev;   
        prev = curr;        
        curr = next;        
    }

    return prev; 
}

<img width="1901" height="859" alt="image" src="https://github.com/user-attachments/assets/d01dbf77-b9c0-4991-ab53-3b43b31cea13" />
