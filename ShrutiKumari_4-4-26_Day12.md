/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 */
bool isPalindrome(struct ListNode* head) {
        int arr[100000]; 
    int size = 0;

    struct ListNode* temp = head;
    while (temp != NULL) {
        arr[size++] = temp->val;
        temp = temp->next;
    }
    int left = 0, right = size - 1;
    while (left < right) {
        if (arr[left] != arr[right]) {
            return false;
        }
        left++;
        right--;
    }

   <img width="1902" height="861" alt="image" src="https://github.com/user-attachments/assets/b5732454-1a40-43f5-b413-259729b09ec4" />
