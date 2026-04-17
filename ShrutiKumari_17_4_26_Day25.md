int max(int a, int b) {
    return (a > b) ? a : b;
}

int height(struct TreeNode* root, int* diameter) {
    if (root == NULL)
        return 0;

    int left = height(root->left, diameter);
    int right = height(root->right, diameter);

    if (left + right > *diameter)
        *diameter = left + right;

    return max(left, right) + 1;
}

int diameterOfBinaryTree(struct TreeNode* root) {
    int diameter = 0;
    height(root, &diameter);
    return diameter;
}
<img width="1901" height="859" alt="image" src="https://github.com/user-attachments/assets/a0adbfce-5bd5-4c7f-88c0-cc9bd192555a" />
