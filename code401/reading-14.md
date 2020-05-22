# Binary Trees

- Terminology
  - Node: A node is the individual item/data that makes up the data structure
  - Root: The root is the first/top Node in the tree
  - Left Child: The node that is positioned to the left of a root or node
  - Right Child: The node that is positioned to the right of a root or node
  - Edge: The edge in a tree is the link between a parent and child node
  - Leaf: A leaf is a node that does not contain any children
  - Height: The height of a tree is determined by the number of edges from the root to the bottommost node
  - *Binary* trees can only have two children per node

- Travesal
  - many different methods
  - uses recursion to add nodes to call stack
  - Depth first
    - prioritzing traveling through the depth/height of the tree. 
    - Pre-order: Root -> Left -> Right
      - Algorithm preOrder(root)
        output <- root.value
        if root.left is not Null preOrder(root.left)
        if root.right is not Null preOrder(root.right)
    - In-Order: left -> root -> right
      - Algorithm inOrder(node)
        if node.left is not null: inOrder(node.left)
        Output <- node.value
        if node.right is nut null: inOrder(node.right)
    - Post-order: left -> right -> root
       - Algorithm postOrder(node)
        if node.left is not null: postOrder(node.left)
        if node.right is nut null: postOrder(node.right)
         Output <- node.value
   - Breadth First
     - iterates through the tree by going through each level of the tree node by node
     - uses a queue
     - Algorithm: breadthFirst(root)
       Queue Breadth <- new Queue
       Breadth.enqueue(root)

       while breadth.peek()
          node front = breadth.dequeue
          Output <- front.value

          if front.left is not null: breadth.enqueue(front.left)
          if. front.right is not null: breadth.enqueue(front.right)