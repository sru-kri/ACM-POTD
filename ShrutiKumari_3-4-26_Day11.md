/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 */
struct ListNode *getIntersectionNode(struct ListNode *headA, struct ListNode *headB) {
    if (headA == NULL || headB == NULL) {
        return NULL;
    }

    struct ListNode *ptrA = headA;
    struct ListNode *ptrB = headB;

    while (ptrA != ptrB) {
        if (ptrA == NULL) {
            ptrA = headB;  
        } else {
            ptrA = ptrA->next;
        }
        if (ptrB == NULL) {
            ptrB = headA;  
        } else {
            ptrB = ptrB->next;
        }
    }

    return ptrA;
}

<img width="1898" height="858" alt="Screenshot 2026-04-03 130334" src="https://github.com/user-attachments/assets/60bfa603-7b88-47a0-9cba-12af55ba3b27" />
