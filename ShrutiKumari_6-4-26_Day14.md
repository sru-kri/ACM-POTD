#define MAX 100
typedef struct {
    int s1[MAX];
    int s2[MAX];
    int top1;
    int top2;
} MyQueue;

MyQueue* myQueueCreate() {
    MyQueue* obj = (MyQueue*)malloc(sizeof(MyQueue));
    obj->top1 = -1;
    obj->top2 = -1;
    return obj;
}

void myQueuePush(MyQueue* obj, int x) {
    obj->s1[++(obj->top1)] = x;  
}
void transfer(MyQueue* obj) {
    if (obj->top2 == -1) {
        while (obj->top1 != -1) {
            obj->s2[++(obj->top2)] = obj->s1[(obj->top1)--];
        }
    }
}
int myQueuePop(MyQueue* obj) {
    transfer(obj);
    return obj->s2[(obj->top2)--];
}

int myQueuePeek(MyQueue* obj) {
    transfer(obj);
    return obj->s2[obj->top2];
}

bool myQueueEmpty(MyQueue* obj) {
    return (obj->top1 == -1 && obj->top2 == -1);
}

void myQueueFree(MyQueue* obj) {
    free(obj);
}

/**
 * Your MyQueue struct will be instantiated and called as such:
 * MyQueue* obj = myQueueCreate();
 * myQueuePush(obj, x);
 
 * int param_2 = myQueuePop(obj);
 
 * int param_3 = myQueuePeek(obj);
 
 * bool param_4 = myQueueEmpty(obj);
 
 * myQueueFree(obj);

*/
<img width="1911" height="859" alt="image" src="https://github.com/user-attachments/assets/7887b284-11e3-4fcc-b93b-08386d754fce" />
