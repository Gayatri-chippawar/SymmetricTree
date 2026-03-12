# 🌳 Symmetric (Mirror) Binary Tree – Java

## 📌 Overview

This project demonstrates how to check whether a **Binary Tree is symmetric (mirror of itself)** using **recursion in Java**.

A binary tree is called **symmetric** if the **left subtree is a mirror reflection of the right subtree**.

This is a commonly asked **Binary Tree interview problem** and helps in understanding **tree recursion and structural comparison**.

---

# 🌿 Example Tree

Example of a **symmetric binary tree**:

```id="tree_sym"
        1
       / \
      2   2
     / \ / \
    3  4 4  3
```

The left subtree is the **mirror image** of the right subtree.

Output:

```id="sym_out"
true
```

---

# ❌ Example of Non-Symmetric Tree

```id="tree_nonsym"
        1
       / \
      2   2
       \   \
        3   3
```

Output:

```id="nonsym_out"
false
```

---

# 🎯 Problem Statement

Given the **root of a binary tree**, determine whether the tree is **symmetric around its center**.

---

# ⚙️ Algorithm

The solution uses **recursion** to compare nodes in a mirrored way.

### Steps

1️⃣ If the root is `null`, the tree is symmetric.
2️⃣ Compare the **left subtree** and **right subtree**.
3️⃣ Two nodes are mirrors if:

* Their values are equal.
* The **left child of one equals the right child of the other**.
* The **right child of one equals the left child of the other**.

---

# 💻 Java Implementation

### Check if Tree is Symmetric

```java id="code_sym1"
public boolean isSymmetric(Node root) {
    if(root == null){
        return true;
    }
    return isMirror(root.left, root.right);
}
```

---

### Mirror Comparison Function

```java id="code_sym2"
public boolean isMirror(Node left, Node right) {

    if(left == null && right == null){
        return true;
    }

    if(left == null || right == null){
        return false;
    }

    if(left.data != right.data){
        return false;
    }

    return isMirror(left.left, right.right) &&
           isMirror(left.right, right.left);
}
```

---

# ▶️ Program Output

```id="sym_output"
true
```

The given tree is **symmetric**.

---

# ⏱ Time and Space Complexity

| Complexity       | Value |
| ---------------- | ----- |
| Time Complexity  | O(n)  |
| Space Complexity | O(h)  |

Where:

* **n** = number of nodes in the tree
* **h** = height of the tree (recursion stack)

---

# 🧠 Concepts Used

* 🌳 Binary Trees
* 🔁 Recursion
* 🔍 Tree Traversal
* 🪞 Mirror Tree Concept
* 🧩 Structural Comparison

---

# 🎯 Learning Outcomes

After completing this program you will understand:

✔ What a **symmetric binary tree** is
✔ How to compare mirrored nodes recursively
✔ How recursion works in tree problems
✔ Binary tree structure analysis

These concepts are essential for **Data Structures and Algorithms (DSA)** and **technical interviews**.

---

# 👨‍💻 Author

Developed as part of **Data Structures and Algorithms practice** 🚀
