Task: Given the pointer root (which points to the root of a given binary search tree), create a function which returns the height of that binary search tree.

Solution:
```javascript
 if (root == null) {
 	return -1;
 }
 return 1 + Math.max(this.getHeight(root.left), this.getHeight(root.right));
 ```
