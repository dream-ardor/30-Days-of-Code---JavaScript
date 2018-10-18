Task: Given a node object with integer data field data, and instance pointer next which points to the next node, you’ll need to use the removeDuplicates function to delete any duplicate nodes within the list and then return the head of the newly updated list.

Solution: 
```javascript
    this.removeDuplicates=function(head){
      var prev = head;
        while (prev) {
            var next = prev.next;
            if (next && prev.data == next.data) { 
                prev.next = next.next; 
            } else {
                prev = prev.next;
            }
        }
    return head;
}
```
