struct TreeNode* invertTree(struct TreeNode* root) {
    if (root == NULL) {
        return NULL;
    }

    struct TreeNode* temp = root->left;
    root->left = root->right;
    root->right = temp;

    invertTree(root->left);
    invertTree(root->right);

    return root;    
}

<img width="1889" height="858" alt="image" src="https://github.com/user-attachments/assets/c8d385d7-ea31-42f4-883e-9ba949bd32bc" />
