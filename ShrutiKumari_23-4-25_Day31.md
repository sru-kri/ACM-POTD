int minCostClimbingStairs(int* cost, int costSize) {
    int first = cost[0];
    int second = cost[1];

    for (int i = 2; i < costSize; i++) {
        int current;

        if (first < second)
            current = cost[i] + first;
        else
            current = cost[i] + second;

        first = second;
        second = current;
    }

    if (first < second)
        return first;
    else
        return second;    
}

<img width="1905" height="864" alt="image" src="https://github.com/user-attachments/assets/9bfa7114-e337-4263-9370-4ee803be9591" />
