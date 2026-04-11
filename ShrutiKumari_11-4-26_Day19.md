char* makeGood(char* s) {
    int n = strlen(s);
    char* result = (char*)malloc((n + 1) * sizeof(char));
    
    int top = -1;
    for (int i = 0; i < n; i++) {
        if (top >= 0 && abs(result[top] - s[i]) == 32) {
            top--; 
        } else {
            top++;
            result[top] = s[i]; 
        }
    }

    result[top + 1] = '\0'; 
    return result;
}

<img width="1903" height="859" alt="image" src="https://github.com/user-attachments/assets/4c4fca38-c238-4139-91f7-bbf6793bc916" />
