int maxDepth(struct TreeNode* root) {
    if (root == NULL) {
        return 0;
    }

    int left = maxDepth(root->left);
    int right = maxDepth(root->right);

    if (left > right) {
        return left + 1;
    } else {
        return right + 1;
    }    
}

<img width="1901" height="860" alt="image" src="https://github.com/user-attachments/assets/a70d1ba5-3053-4d8d-b37b-94e6fdd33b6a" />
