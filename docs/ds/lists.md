### Lists

#### vector

#### list


### Stacks

Clearly `list` and `vector` support stack operations; 99% of the time they are the most reasonable choice.

- Stack model
  
  Stacks are known as LIFO (last in, first out).  
  Input to a stack is by push; output is by pop and top.  
  Only the top element is accessible.  

#### Applications

- Balancing Symbols

  Make an empty stack. Read characters untile end of file.  
  If the character is an opening symbol, push it onto the stack. If it is a closing symbol and the stack is empty, report an error. Otherwise, pop the stack.  
  If the symbol is not the corresponding opening symbol, then report an error.  
  At the end of file, if the stack is not empty, report an error.

- Postfix Expressions
- Infix to Postfix Conversion
- Function Calls

### Queues

- Queue Model

  The basic operations on a queue are `enqueues`, which inserts an element at the end of list (called the rear).  
  and `dequeue`, which deletes (and returns) the element at the start of the list (known as the front).
