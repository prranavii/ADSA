## STACK USING LINKEDLIST GFG PRACTICE 

```JAVA
// Node class
/* class Node {
    int data;
    Node next;

    Node(int new_data) {
        data = new_data;
        next = null;
    }
} */

// Stack class
class myStack {
    
    private Node top;
    private int size;
    

    public myStack() {
        // Initialize your data members
        top = null;
        size=0;
        
    }

    public boolean isEmpty() {
        // check if the queue is empty
        return top == null;
    }

    public void push(int x) {
        // Adds an element x at the rear of the queue.
        Node newNode = new Node (x);
        newNode.next = top;
        top = newNode;
        size++;
    }

    public void pop() {
        // Removes the front element of the queue
        if(isEmpty()){
            return;
        }
        top=top.next;
        size--;
        
    }

    public int peek() {
        // Returns the front element of the queue.
        // If queue is empty, return -1.
        if(isEmpty()){
            return -1;
        }
        return top.data;
    }

    public int size() {
        // Returns the current size of the queue.
        return size;
    }
}
