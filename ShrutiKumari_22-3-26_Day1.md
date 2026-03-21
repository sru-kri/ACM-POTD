int removeDuplicates(int* nums, int numsSize) {
    if (numsSize == 0) return 0;

    int i = 0, j = 1;

    while (j < numsSize) {
        if (nums[j] != nums[i]) {
            i++;
            nums[i] = nums[j];
        }
        j++;
    }

    return i + 1;
}

<img width="1262" height="794" alt="Screenshot 2026-03-22 011330" src="https://github.com/user-attachments/assets/5c9d1d51-4639-4c20-be6e-99356910b85a" />
