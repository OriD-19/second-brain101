The trick for this problem is to keep track of the minimum values of the stack THROUGH THE HISTORY of the operations.

That means that we only care about the values that were a minimum at SOME POINT of the history of operations. The rest, we don't care about, since they are going to be excluded anyways.

We have to keep track of two stacks:
- One regular stack for the normal operations of "stacking" the elements.
- Another one that keeps track of the history of min values.

> Important concept: JUST KEEP TRACK OF THE INFORMATION THAT WE CARE ABOUT. Don't mind the rest of the data that we are not going to use for anything!

Code:
```cpp
class MinStack {
public:

    stack<int> container;
    stack<pair<int, int>> min_container;

    MinStack() {
        
    }
    
    void push(int val) {
        this->container.push(val);

        if(this->min_container.empty() || val < this->min_container.top().first) 
            this->min_container.push({val, 1});
        else if(val == this->min_container.top().first)
            this->min_container.top().second++;
    }
    
    void pop() {
        if(this->container.top() == this->min_container.top().first)
            this->min_container.top().second--;
            if(this->min_container.top().second == 0)
                this->min_container.pop();
        
        this->container.pop();
    }
    
    int top() {
        return this->container.top();     
    }
    
    int getMin() {
        return this->min_container.top().first; 
    }
};
```