# Experiment-18

## AIM
To learn queue in c++.

## Poblem Statement
Write a program to dequeue & enqueue in c++.

# Theory
A queue is a way to arrange items so that the first item you put in is the first one you take out, which is known as first-in, first-out (FIFO). You place new items at the back of the queue and remove items from the front. Queues are useful in everyday situations, like waiting in line at a store or managing tasks in a computer program. They have basic actions, such as adding an item (called enqueue) and removing an item (called dequeue). You can create queues using lists or other special structures, which make it easy to add and remove items quickly.

## Program Codes
```javascript
// Sharvari Murade
//23070123088
#include <iostream>
using namespace std;
#define size 5
#define ERROR -9999
class Queue{
    int rear, front, ar[size];
    public:
    Queue(){
        rear = -1;
        front = -1;
        ar[0]=0;
    }
    void enqueue(int);
    int dequeue();
    void disp();
};
void Queue :: enqueue(int num){
    if (rear == (size+1)){
        cout<<"Queue is full"<<endl;
    }
    else{
        if(front == -1){
            ar[++front]=num;
            rear++;
        }
        else{
            ar[++rear]=num;
        }
    }

    }
int Queue ::dequeue(){
    if(front ==-1 || front ==(rear+1)){
        cout<<"Queue is empty"<<endl;
        return ERROR;
    }
    else{
        int val = ar[front++];
        return val;
    }
}
void Queue :: disp(){
    if(front ==-1 || front ==(rear+1)){
        cout<<"Quee=ue is empty"<<endl;
        return;
    }
    else{
        int i = front ;
        while (i!=(rear+1)){
            cout<<ar[i];
            i++;
        }
    }
}

int main(){
        Queue q1;
        q1.enqueue(4);
        q1.enqueue(8);
        q1.enqueue(3);
        q1.disp();
        int val = q1.dequeue();
        cout<<endl<<"Deleted element: "<<val<<endl;
        q1.disp();

}
```

## Program Output 
<img width="324" alt="image" src="https://github.com/user-attachments/assets/d5cf660d-8709-4fd7-a081-5bf1397ca2cc">

## Conclusion 
In summary, queues are a simple and effective way to manage items in the order they arrive. Their first-in, first-out structure makes them suitable for various real-life situations and computer applications, allowing for efficient organization and quick processing of tasks.

