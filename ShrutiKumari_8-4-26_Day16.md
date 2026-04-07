char* removeDuplicates(char* s) {
        int i = 0;  

    for (int j = 0; s[j] != '\0'; j++) {
        if (i > 0 && s[i - 1] == s[j]) {
            i--; 
        } else {
            s[i] = s[j];  
            i++;
        }
    }

    s[i] = '\0'; 
    return s;
}
<img width="1901" height="865" alt="image" src="https://github.com/user-attachments/assets/eac2cbb7-e914-4775-a72e-7333c00288e3" />
