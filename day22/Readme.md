235
BST的LCA，这一题需要利用BST的特性，之前普通树的回溯递归是从下往上遍历，所以判断方法是不同的。这棵树是从上往下遍历，可以通过走一些例子发现，当我们遇到第一个节点左子树有q,右子树有p的时候，这个节点就是LCA。
所以无论是递归还是迭代，都是从上往下遍历，如果root.val在这个区间，那么就返回这个值，如果不是的话那么就通过左移或者右移root来实现。
701
二叉树中的插入操作。
二叉树插入操作可以选择一个不改变树结构的方法来插入这个节点。就是通过在左右子树之间移动，找到一个合理的空位置直接插入就好。如果当前节点为空，就可以直接构建一个新节点返回。
如果当前val比较大，就可以选择右结点来接住这个返回值，比较小的话就选择左结点来接住这个返回值。最后返回root。
450
删除节点操作。
跟插入结点的操作一样，当val没找到的时候，就是用左结点或者右结点来接住这个函数的返回值。当找到之后有几种操作：
1. 当是叶子结点的话，那么就直接返回空
2. 当左右结点其中一个几点为空的话，就拿左结点或者右结点取代当前这个父节点
3. 当左结点和右结点都不为空的时候，要先找到右子树的最左边这个节点。然后把左子树都移到这个节点下面，这样没有改变BST的规则，然后返回这个右子树的根节点即node.right.
   


