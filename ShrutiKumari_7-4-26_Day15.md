#define MAX 100 

typedef struct {
        int data[MAX];
    int front, rear;
} Queue;

void initQueue(Queue* q) {
    q->front = 0;
    q->rear = 0;
}

bool isEmptyQueue(Queue* q) {
    return q->front == q->rear;
}

void enqueue(Queue* q, int x) {
    if (q->rear < MAX) {
        q->data[q->rear++] = x;
    }
}

int dequeue(Queue* q) {
    if (!isEmptyQueue(q)) {
        return q->data[q->front++];
    }
    return -1; 
}

typedef struct {
    Queue q1, q2;
} MyStack;


MyStack* myStackCreate() {
        MyStack* stack = (MyStack*)malloc(sizeof(MyStack));
    initQueue(&stack->q1);
    initQueue(&stack->q2);
    return stack;
}

void myStackPush(MyStack* obj, int x) {
       enqueue(&obj->q2, x);

    while (!isEmptyQueue(&obj->q1)) {
        enqueue(&obj->q2, dequeue(&obj->q1));
    }

    Queue temp = obj->q1;
    obj->q1 = obj->q2;
    obj->q2 = temp;
}

int myStackPop(MyStack* obj) {
    return dequeue(&obj->q1);
}

int myStackTop(MyStack* obj) {
    if (!isEmptyQueue(&obj->q1)) {
        return obj->q1.data[obj->q1.front];
    }
    return -1;
}

bool myStackEmpty(MyStack* obj) {
    return isEmptyQueue(&obj->q1);
}

void myStackFree(MyStack* obj) {
    free(obj);
}

/**
 * Your MyStack struct will be instantiated and called as such:
 * MyStack* obj = myStackCreate();
 * myStackPush(obj, x);
 
 * int param_2 = myStackPop(obj);
 
 * int param_3 = myStackTop(obj);
 
 * bool param_4 = myStackEmpty(obj);
 
 * myStackFree(obj);

*/
<img width="1896" height="858" alt="image" src="https://github.com/user-attachments/assets/7e4afc2c-75cb-46a2-933d-59bc32f47651" />
