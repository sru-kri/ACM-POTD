bool backspaceCompare(char* s, char* t) {
        char resultS[201], resultT[201];
    int i, j;
    for (i = 0, j = 0; s[i] != '\0'; i++) {
        if (s[i] == '#') {
            if (j > 0) j--;
        } else {
            resultS[j++] = s[i];
        }
    }
    resultS[j] = '\0';
    for (i = 0, j = 0; t[i] != '\0'; i++) {
        if (t[i] == '#') {
            if (j > 0) j--;
        } else {
            resultT[j++] = t[i];
        }
    }
    resultT[j] = '\0';
    return strcmp(resultS, resultT) == 0;
}

<img width="1905" height="864" alt="image" src="https://github.com/user-attachments/assets/aeb8da45-f080-4027-8eff-291bb0a1faf3" />
