[[二叉树基础]]

  

- 遍历方法
    
    - Involve backtracing of the value from subtrees, usually some sums.
    - Involve special base case that terminate before reaching null.
    - Remember, the value is either generated by base case, or special base case originally, parents node depend on those original values
    
    [[DFS using recursion]]
    
    [[DFS using stack]]
    
    [[102. Binary Tree Level Order Traversal (BFS)]]
    

  

- 求值（后序）
    
    [[104. Maximum Depth of Binary Tree]]
    
    [[111. Minimum Depth of Binary Tree]]
    
    [[404. Sum of Left Leaves]]
    
    [[222. Count Complete Tree Nodes]]
    
      
    
- 判断
    
    - For all correctness checking problem, the correctness of a node depends on
        1. The corretness of the node itself
        2. The correctness of left subtree
        3. The correctness of right subtree
    - It **always** involves a **post-order** traversal for collecting validness of both subtrees
    - Usually after collecting validness of subtrees, you will check the validness of current root and then return the validness of subtrees.
        - Except for this problem 98 Validate Binary Search Tree. We must put the checking for current root in the middle of two traversals to utilize the characteristics of in-order traversal
    - The process of collecting boolean from subtrees is actually backtracing
    - Remember, the value is either generated by base case, or special base case originally, parents node depend on those original values
    
    [[101. Symmetric Tree]]
    
    [[110. Balanced Binary Tree]]
    
    [[98. Validate Binary Search Tree]]
    
    [[112. Path Sum]]
    
      
    
- 路径
    
    - 与路径相关的题，base case必须是叶子节点。如果base case设在null的话，会记录很多不合法的路径
        
        ![[Untitled.jpeg]]
        
        - 蓝色是一条路径，红色不是一条路径。但base case为null的话，会把红色算作一条路径
    - 这带来一系列后果，首先因为base case不是null了，所以左右节点有可能是null，所以必须搭配 `node.left != null` 和 `node.right != null` 食用。同时，必须保证root在进入递归前不为null
    - 路径类题一般用前序遍历（一边探索一边收集），因为base case变为叶子节点了，为了不落下叶子节点，中（收集）一般放在base case前面。或者你也可以base case里面放一个，紧跟着base case再放一个，但这样会造成两行一摸一样的代码，冗余。
    
    [[257. Binary Tree Paths]]
    
    [[112. Path Sum]]
    
      
    
- 层序
    
    [[513. Find Bottom Left Tree Value]]
    
      
    
- 构造二叉树
    
    - Involves backtracing for `root->left` and `root->right`
    - Processing mid (creating root) can be placed anywhere actually, so not necessarily post-order traversal
    
    [[106. Construct Binary Tree from Inorder and Postorder Traversal]]
    
    [[654. Maximum Binary Tree]]
    
    [[108. Convert Sorted Array to Binary Search Tree]]
    
    [[617. Merge Two Binary Trees]]
    
      
    
- 公共祖先
    
    - Involves backtracing to transmit founded ancestor/target
    - Involves a special base case that terminates before reaching null when discovering target/ancestor
    
    [[236. Lowest Common Ancestor of a Binary Tree]]
    
    [[235. Lowest Common Ancestor of a Binary Search Tree]]
    
      
    
- BST双指针
    
    - In-order traversal to sorted array
    - Can be ascending and descending
    
    [[98. Validate Binary Search Tree]]
    
    [[530 Minimum Absolute Difference in BST]]
    
    [[501. Find Mode in Binary Search Tree]]
    
    [[538. Convert BST to Greater Tree]]
    
      
    
- BST修改（插入/删除）
    
    [[701. Insert into a Binary Search Tree]]
    
    [[450. Delete Node in a BST]]
    
    [[669. Trim a Binary Search Tree]]
    
      
    
- 我也不知道搁哪好
    
    [[226. Invert Binary Tree]]
    
    [[700. Search in a Binary Search Tree]]