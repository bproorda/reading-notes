# Stacks and Queues

**Stack**
- a *stack* is data structure of nodes where is each node has a reference to the next
- push: a node is added to top of the top of the stack
- pop: a node is removed from the top of the stack
- peek: checks the value of the top node of the stack
- isEmpty: method that returns true if the stack is empy
- FILO: the first node in the stack is the  last one out
- LIFO: the  last node in the stack is the first one out
- the last node is refered to as the *top*
- pushing a node is a O(1) operation
   - 1. create new node
   - 2. set new nodes next reference to the current top
   - 3. reassign top reference to the new node
   - node = new Node(value)
   - node.next <= Top
   - Top <= node 
- pop is also O(1)
  - 1. check isEmpty to prevent exception
  - 2. create temp node that points to the same node as top does
  - 3. reassign top to top.next
  - 4. set temp.next to null
  - 5. return temp.value
- peek O(1) returns top.value


**Queues**
- a *queue is a data structure
- enqueue: nodes are added to the queue
- dequeue: nodes are removed from the queue
- front: the first node in the queue
- back: the last node in the queue
- First in First out
- Last  in  Last out
- enqueue O(1)
  - node = new Node(value)
  - rear.next <= node
  - rear <= node
- dequeue
  - Node temp = front
  - front <= front.next
  - temp.next = null
- peak returns front.value