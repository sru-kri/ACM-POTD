int missingNumber(int* nums, int numsSize) {
    int total = 0;
    int i;
    for (i = 0; i <= numsSize; i++) {
        total += i;
    }
    for (i = 0; i < numsSize; i++) {
        total -= nums[i];
    }
    return total;
}

<img width="1902" height="860" alt="Day4" src="https://github.com/user-attachments/assets/dd3219f6-4632-4dc2-9f25-53270d3532e0" />

