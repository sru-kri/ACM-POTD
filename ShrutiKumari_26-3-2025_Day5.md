void moveZeroes(int* nums, int numsSize) {
    int i, j = 0;

    for (i = 0; i < numsSize; i++) {
        if (nums[i] != 0) {
            nums[j] = nums[i];  
            j++;             
        }
    }
    for (i = j; i < numsSize; i++) {
        nums[i] = 0;
    }
}

<img width="1896" height="862" alt="Day5" src="https://github.com/user-attachments/assets/b4581ceb-ceb2-486b-95fd-549d45ae1fd9" />
