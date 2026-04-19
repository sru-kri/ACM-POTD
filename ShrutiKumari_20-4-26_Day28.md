bool isPowerOfTwo(int n) {
    if (n <= 0) {
        return false;
    }
    while (n % 2 == 0) {
        n = n / 2;
    }
    return n == 1;
}

<img width="1896" height="861" alt="image" src="https://github.com/user-attachments/assets/51409584-af45-4f41-a6f1-1cd937b1b79c" />
