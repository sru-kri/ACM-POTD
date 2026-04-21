int lengthOfLIS(int* nums, int numsSize) {
    int dp[numsSize];
    int maxLen = 1;
    for (int i = 0; i < numsSize; i++) {
        dp[i] = 1;
    }
    for (int i = 1; i < numsSize; i++) {
        for (int j = 0; j < i; j++) {
            if (nums[j] < nums[i]) {
                if (dp[j] + 1 > dp[i]) {
                    dp[i] = dp[j] + 1;
                }
            }
        }
        if (dp[i] > maxLen) {
            maxLen = dp[i];
        }
    }
    return maxLen;    
}

<img width="1902" height="860" alt="image" src="https://github.com/user-attachments/assets/88d13b27-2fc0-41f2-b34d-276d39d46275" />
