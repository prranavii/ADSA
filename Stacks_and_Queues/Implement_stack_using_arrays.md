## Implement stack using arrays GFG PRACTICE



```java
class myStack {
    
     private int [] data;
        private int ptr=-1;

    public myStack(int n) {
        // Define Data Structures
          data = new int[n];
    }

    public boolean isEmpty() {
        // check if the stack is empty
       return ptr == -1;
    }

    public boolean isFull() {
        // check if the stack is full
       return ptr == data.length-1;
    }

    public void push(int x) {
        // Inserts x at the top of the stack
        if(isFull()){
            
            return ;
        }
        ptr++;
        data[ptr]=x;
        
    }

    public void pop() {
        // Removes an element from the top of the stack
        if(isEmpty()){
            return;
        }
        ptr--;
    }

    public int peek() {
        // Returns the top element of the stack
        if(isEmpty()){
            return -1;
        }
        return data[ptr];
    }
}
