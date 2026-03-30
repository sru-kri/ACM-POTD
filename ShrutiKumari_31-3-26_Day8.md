/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 */
struct ListNode* middleNode(struct ListNode* head) {

    struct ListNode *slow = head;
    struct ListNode *fast = head;

    while (fast != NULL && fast->next != NULL) {
        slow = slow->next;          
        fast = fast->next->next;   
    }

    return slow;
}

<img width="1902" height="852" alt="image" src="https://github.com/user-attachments/assets/8b5ac542-8ae8-40bd-b984-f4e78b52fa01" />
