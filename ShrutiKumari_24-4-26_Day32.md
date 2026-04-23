int rob(int* nums, int numsSize) {
    int prev1 = 0; 
    int prev2 = 0; 
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

<img width="1900" height="856" alt="image" src="https://github.com/user-attachments/assets/4f7ea596-f02b-4d37-ad4c-0060bd5c3419" />
