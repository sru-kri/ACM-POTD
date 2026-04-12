 void dfs(int** image, int m, int n, int r, int c, int orig, int color) {
    if (r < 0 || r >= m || c < 0 || c >= n) return;
    if (image[r][c] != orig) return;

    image[r][c] = color;

    dfs(image, m, n, r+1, c, orig, color);
    dfs(image, m, n, r-1, c, orig, color);
    dfs(image, m, n, r, c+1, orig, color);
    dfs(image, m, n, r, c-1, orig, color);
}

int** floodFill(int** image, int imageSize, int* imageColSize, int sr, int sc, int color, int* returnSize, int** returnColumnSizes) {
    int orig = image[sr][sc];

    if (orig == color) {
        *returnSize = imageSize;
        *returnColumnSizes = imageColSize;
        return image;
    }

    <img width="1900" height="867" alt="image" src="https://github.com/user-attachments/assets/adb23114-db28-45c4-9982-a60a5ec214e9" />
