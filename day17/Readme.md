110
平衡二叉树，这一题就是求两边树的高度，递归的话，就是用一个helper function分别求两边子树的高度。这种有返回值的求树的高度的，当要判断false的时候可以返回一个负数。
257
求出一棵树的每个路径。这个题目要注意的就是到最后一个节点的时候就不需要箭头了，所以要单独处理，而不是到了跟节点的时候再处理，而是在根结点的父节点的时候再处理。为了避免回溯，
不是直接对传入的参数s进行改变。
404
求左叶子节点的和，递归和迭代类似，都是在左叶子节点的上一层也就是父节点的时候进行判断。