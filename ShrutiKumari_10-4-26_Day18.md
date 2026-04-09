char* removeOuterParentheses(char* s) {
    int n = strlen(s);
    char* result = (char*)malloc((n + 1) * sizeof(char)); 

    int depth = 0;
    int j = 0;

    for (int i = 0; i < n; i++) {
        if (s[i] == '(') {
            if (depth > 0) {
                result[j++] = '(';
            }
            depth++;
        } else {
            depth--;
            if (depth > 0) {
                result[j++] = ')';
            }
        }
    }

    result[j] = '\0';
    return result;
}

<img width="1900" height="861" alt="image" src="https://github.com/user-attachments/assets/4bdc1d36-37ad-42f3-9220-1721b898c56e" />
