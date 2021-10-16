# 20211016

# LeetCode 94. Binary Tree Inorder Traversal

  # Definition for a binary tree node.
  # class TreeNode:
    # def __init__(self, val=0, left=None, right=None):
        # self.val = val
        # self.left = left
        # self.right = right
class Solution:
    def inorderTraversal(self, root: Optional[TreeNode]) -> List[int]:
        curr, stack, result = root, [], []
        while curr or stack:
            while curr: 
                stack.append(curr)
                curr = curr.left
            node = stack.pop()
            result.append(node.val)
            curr = node.right
        return result

# 코딩도장 - N-회별문
text = 'hello'
 
two_gram = zip(text, text[1:])
for i in two_gram:
    print(i[0], i[1], sep='')

[변수]
1. 변수 선언하기
    x, y, z = 10, 20, 30
2. 변수 삭제, 리스트에서 유용
    del x 변수 삭제, 리스트에서 유용
3. 빈 변수 선언 None
    x = None
    

