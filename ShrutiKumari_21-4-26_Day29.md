int climbStairs(int n) {
    if (n == 1) return 1;
    if (n == 2) return 2;

    int first = 1;  
    int second = 2;  
    int current;

    for (int i = 3; i <= n; i++) {
        current = first + second;
        first = second;
        second = current;
    }

    return second;    
}

<img width="1902" height="862" alt="image" src="https://github.com/user-attachments/assets/b481bafd-5df6-4b5e-a032-03d0ec56c34d" />
