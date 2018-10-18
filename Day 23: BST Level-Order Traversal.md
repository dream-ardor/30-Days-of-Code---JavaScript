Task: To perform a level-order traversal (also known as a breadth-first search, or BFS) on a given binary tree. We are given the pointer root and asked to create a function which prints out the level-order traversal of the binary tree with a space between each value.

Solution:
```javascript
var queue = [root];
while (queue.length) {
	var treeNode = queue.shift();
	process.stdout.write(treeNode.data + ' ');
	if (treeNode.left) {
		queue.push(treeNode.left);
	}
	if (treeNode.right) {
		queue.push(treeNode.right);
	}
}
```
