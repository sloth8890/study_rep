# Java Cheat Sheet
##  Introduction
I prepared Coding Test using Java8 for the Backend Role. I have a proficient experience in Gradle Build Tool, SpringBoot (RESTAPI), JavaFx, Processing, and jQuery.
In this cheat sheet, I wrote some useful operations for reminding java syntaxes, and operations for the coding test.  
## Lambda Expression

```java
int (int a, int b) {
 return a > b ? a : b;
}
```
Above statement can be deducted by following processes.
```java
(int a, int b) -> {return a > b ? a : b};
```

```java
(int a, int b) -> a > b ? a : b;
```

```java
(a, b) -> a > b ? a : b;
```
Reminds that if there is more than one parameter then bracket is **necessary**

| Method | Lambda Expression |
| ---- | ---- |
| void printVal(String name, int i) {<br>System.out.println(name + "=" + i);<br>} | (name, i) -> System.out.println(name + "=" + i) |
| int roll() {<br>return (int) (Math.random() * 6)<br>} | () -> {return (int) (Math.random() * 6);} |
[More Syntaxes for Lambda Expression](https://hstory0208.tistory.com/entry/Java%EC%9E%90%EB%B0%94-%EB%9E%8C%EB%8B%A4%EC%8B%9DLambda%EC%9D%B4%EB%9E%80-%EA%B7%B8%EB%A6%AC%EA%B3%A0-%EC%82%AC%EC%9A%A9%EB%B2%95)


## Array Operations
### Obtaining Array Length
```java
int[] arr = { 1, 2, 3 };
int arrL = arr.length;
```
### Using stream convert an Array to a List
To solve array question, converting array to list helps to solve the question more efficiently.
Using stream

```java
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class IntArrayConvertToList {
    public static void main(String[] args) {
        // int array
        int[] arr = { 1, 2, 3 };

        // int -> List
        List<Integer> intList 
                = Arrays.stream(arr)
                        .boxed()
                        .collect(Collectors.toList());

        // print List
        System.out.println(intList.size()); // 3
        System.out.println(intList); // [1, 2, 3]
    }
}
```

### Using Arrays.fill() in Java
```java
// Java program to fill a subarray array with` 
// given value.`
import java.util.Arrays;

public class Main{
	public static void main(String[] args) {
		int arr[] = {1, 2, 3, 4, 5, 6, 7, 8, 9};
		// Fill from index 1 to 4 by 10;
		Arrays.fill(arr, 1, 5, 10);
		System.out.println(Arrays.toString(ar));
	}
}
```
Output would be like
```
[1, 10, 10, 10, 10, 6, 7, 8, 9]
```

## LinkedList and Queue

To implement BFS, DFS and other algorithms, Queue/LinkedList data structures are strongly recommended to traverse the nodes.


- Basic usage of LinkedList and Queue. 
```java
import java.util.LinkedList;
import java.util.Queue;

public class QueueAndLinkedListExample {

    public static void main(String[] args) {
        // Create a linked list
        LinkedList<String> linkedList = new LinkedList<>();

        // Add elements to the linked list
        linkedList.add("Apple");
        linkedList.add("Banana");
        linkedList.add("Orange");

        // Display the linked list
        System.out.println("Linked List: " + linkedList);

        // Create a queue using the linked list
        Queue<String> queue = new LinkedList<>(linkedList);

        // Enqueue (add) elements to the queue
        queue.offer("Grapes");
        queue.offer("Pineapple");

        // Display the elements in the queue
        System.out.println("Queue: " + queue);

        // Dequeue (remove) elements from the queue
        String removedElement = queue.poll();
        System.out.println("Dequeued Element: " + removedElement);

        // Display the updated queue
        System.out.println("Updated Queue: " + queue);
    }
}
```
- Practical usage in BFS question
```java
/**
* Definition for a binary tree node.
* public class TreeNode {
	* int val;
	* TreeNode left;
	* TreeNode right;
	* TreeNode() {}
	* TreeNode(int val) { this.val = val; }
	* TreeNode(int val, TreeNode left, TreeNode right) {
		* this.val = val;
		* this.left = left;
		* this.right = right;
		* }
	* }
*/
**class** Solution {
public List<List<Integer>> levelOrder(TreeNode root) {
	List<List<Integer>> collecs = new ArrayList<>();
	if (root == null) {
		return collecs;
	}
	Queue<TreeNode> q = new LinkedList<>();
	q.add(root);
	while (q.size() != 0) {
		int qSize = q.size();
		List<Integer> newL = new ArrayList<>();
		for(int i = 0; i < qSize; i++) {
			TreeNode cur = q.remove();
			newL.add(cur.val);
			
			if (cur.left != null) {
				q.add(cur.left);
			}
			if (cur.right != null) {
				q.add(cur.right);
			}
		}
		collecs.add(newL);
	}
	return collecs;
	}
}
```