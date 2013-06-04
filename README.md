Balanced-Binary-Tree
====================
class Solution {  
public int maxHeight(TreeNode root) {    
        if (root == null) return 0;    
            
        int left = maxHeight(root.left) + 1;    
        int right = maxHeight(root.right) + 1;    
        return left > right ? left : right;    
    }   
      
   public boolean isBalanced(TreeNode root) {  
        // Start typing your C/C++ solution below  
        // DO NOT write int main() function  
        if (root == null) return true;  
          
      
            int left = maxHeight(root.left);  
            int right = maxHeight(root.right);  
            if (Math.abs(left - right) >= 2)  
                return false;  
            else  
                return isBalanced(root.left) && isBalanced(root.right);  
          
    }  
}; 
