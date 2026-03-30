/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 */
bool hasCycle(struct ListNode *head) {
    if (head == NULL || head->next == NULL) {
        return false;
    }

    struct ListNode *slow = head;
    struct ListNode *fast = head;

    while (fast != NULL && fast->next != NULL) {
        slow = slow->next;          
        fast = fast->next->next;    
        if (slow == fast) {
            return true;
        }
    }
    return false;
}

<img width="1906" height="863" alt="Day7" src="https://github.com/user-attachments/assets/401cc1a9-de09-4bdf-bad5-82cc84b496ea" />
