int findJudge(int n, int** trust, int trustSize, int* trustColSize) {
  int* score = (int*)calloc(n + 1, sizeof(int));

    for (int i = 0; i < trustSize; i++) {
        int a = trust[i][0];
        int b = trust[i][1];

        score[a]--;  
        score[b]++;  
    }

    for (int i = 1; i <= n; i++) {
        if (score[i] == n - 1) {
            free(score);
            return i;
        }
    }
    free(score);
    return -1;   
}

<img width="1889" height="832" alt="image" src="https://github.com/user-attachments/assets/c0fbd325-81a1-40ec-9a65-3c7a92b964f2" />
