bool isValid(char* s) {
        char stack[10000];
    int top = -1;

    for (int i = 0; s[i]; i++) {

        if (s[i] == '(' || s[i] == '{' || s[i] == '[')
            stack[++top] = s[i]; 

        else {
            if (top == -1) return false;

            if ((s[i] == ')' && stack[top] != '(') ||
                (s[i] == '}' && stack[top] != '{') ||
                (s[i] == ']' && stack[top] != '['))
                return false;

            top--;
        }
    }

    return top == -1;
}

<img width="1898" height="857" alt="image" src="https://github.com/user-attachments/assets/834cace4-f281-45b4-aa12-502c71c06a06" />
