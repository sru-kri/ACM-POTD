int rob(int* nums, int numsSize) {
    if (numsSize == 0) return 0;
    if (numsSize == 1) return nums[0];

    int prev2 = 0; 
    int prev1 = 0; 

    for (int i = 0; i < numsSize; i++) {
        int take = nums[i] + prev2; 
        int skip = prev1;        
        int current;
        if (take > skip)
            current = take;
        else
            current = skip;

        prev2 = prev1;
        prev1 = current;
    }

    return prev1;     
}
<img width="1896" height="861" alt="image" src="https://github.com/user-attachments/assets/b086c19f-a609-47cf-b395-e3c122f4b5ba" />
