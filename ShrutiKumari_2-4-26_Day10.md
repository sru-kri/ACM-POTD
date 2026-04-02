/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 */
struct ListNode* deleteDuplicates(struct ListNode* head) {
    if (head == NULL) {
        return head;
    }

    struct ListNode* current = head;
    while (current->next != NULL) {
        
        if (current->val == current->next->val) {
            struct ListNode* temp = current->next;
            current->next = current->next->next;
            free(temp);
        } else {
            current = current->next;
        }
    }

    <img width="1895" height="857" alt="image" src="https://github.com/user-attachments/assets/77aa8d1c-fb4d-4e33-a041-affd92ad6811" />
