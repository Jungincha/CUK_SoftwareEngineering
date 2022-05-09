# 자료구조 10주차

## 이진트리 

### 중위순회, 전위순회, 후위순회
`binaryTree.h`
```c
typedef struct treeNode {
	char data;
	struct treeNode *left;
	struct treeNode *right;
} treeNodeType;

treeNodeType *root;

void initTree() { root = NULL; }

int isEmpty() { return (root == NULL); }

treeNodeType *createTree(char elem_data, treeNodeType *left, treeNodeType *right)
{
	treeNodeType *n = (treeNodeType*)malloc(sizeof(treeNodeType));
	n->data = elem_data;
	n->left = left;
	n->right = right;
	
	return n;
}

void Inorder(treeNodeType *tree_ptr)
{
	if (tree_ptr != NULL)
	{
		Inorder(tree_ptr->left);
		printf("노드의 값은 %c 입니다.\n", tree_ptr->data);
		Inorder(tree_ptr->right);
	}
}

void Postorder(treeNodeType *tree_ptr)
{
	if (tree_ptr != NULL)
	{
		Postorder(tree_ptr->left);
		Postorder(tree_ptr->right);
		printf("노드의 값은 %c입니다.\n", tree_ptr->data);
	}
}

void Preorder(treeNodeType *tree_ptr)
{
	if (tree_ptr != NULL)
	{
		printf("노드의 값은 %c 입니다.\n", tree_ptr->data);
		Preorder(tree_ptr->left);
		Preorder(tree_ptr->right);
	}
}
```
`binaryTree.c`
```c
#include <stdio.h>
#include <stdlib.h>
#include "binaryTree.h"

void main()
{
	treeNodeType *b, *c, *d,  *e, *f;
	
	initTree();
	d = createTree('D', NULL, NULL);
	e = createTree('E', NULL, NULL);
	f = createTree('F', NULL, NULL);
	
	b = createTree('B', d, e);
	c = createTree('C', f, NULL);
	
	root = createTree('A', c, b);
	
	printf("트리를 중위순회합니다.\n");
	Inorder(root);
	
	printf("트리를 전위순회합니다.\n");
	Preorder(root);
	
	printf("트리를 후위순회합니다.\n");
	Postorder(root);
}
```

## 이진탐색트리
`bstree.h`
```c
typedef struct treeNode {
	int key;
	char data;
	struct treeNode *left;
	struct treeNode *right;
} treeNodeType;

treeNodeType *root;

void initTree() { root = NULL; }

int isEmpty() { return (root == NULL); }

treeNodeType *createTree(char elem_data, treeNodeType *left, treeNodeType *right)
{
	treeNodeType *n = (treeNodeType*)malloc(sizeof(treeNodeType));
	n->data = elem_data;
	n->left = left;
	n->right = right;
	
	return n;
}
// 순환적 방법
treeNodeType *searchBST (treeNodeType *bstree, int x)
{
	if (bstree == NULL) return NULL;
	if (bstree->key == x) return bstree;
	if (bstree->key < x)
		return searchBST(bstree->right, x);
	else
		return searchBST(bstree->left, x);
}

// 반복적 방법
treeNodeType *searchBST_iter(treeNodeType *bstree, int x)
{
	while(bstree != NULL) {
		if (bstree->key == x) return bstree;
		if (bstree->key < x)
			bstree = bstree->right;
		else
			bstree = bstree->left;
	}
	return NULL;
}

treeNodeType *insertBST(treeNodeType *bstree, int x)
{
	treeNodeType *newnode;
	
	if (bstree == NULL) {
		newnode = (treeNodeType*)malloc(sizeof(treeNodeType));
		newnode->key = x;
		newnode->left = NULL;
		newnode->right = NULL;
		return newnode;
	}
	else if (x < bstree->key) bstree->left = insertBST(bstree->left, x);
	else if (x > bstree->key) bstree->right = insertBST(bstree->right, x);
	else printf("\n 이미 같은 키가 있습니다.\n");
	
	return bstree;
}

void deleteNode(treeNodeType *bstree, int x)
{
	treeNodeType *parent, *node, *succ, *succ_parent, *child;
	
	parent = NULL;
	node = bstree;
	
	while (node != NULL && node->key != x) {
		parent = node;
		if (x < node->key) node = node->left;
		else node = node->right;
	}
	if (node == NULL) {
		printf("찾는 키가 이진트리에 없습니다.\n");
		return;
	}
	// 단말노드
	if(node->left == NULL && node->right == NULL) {
		if (parent == NULL) root = NULL;
		else {
			if (parent->left == node) parent->left = NULL;
			else parent->right = NULL;
		}
	}
	
	// 자식노드 1개인 경우
	else if (node->left == NULL || node->right == NULL) {
		if (node->left != NULL) child = node->left;
		else child = node->right;
		
		if (parent == NULL) root = child;
		else {
			if (parent->left == node) parent->left = child;
			else parent->right = child;
		}
	} else {
		//  자식노드가 2개인 경우
		succ_parent = node;
		succ = node->left;
		
		while (succ->right != NULL) {
			succ_parent = succ;
			succ = succ->right;
		}
		
		if (succ_parent->left == succ) succ_parent->left = succ->left;
		else succ_parent->right = succ->left;
		
		node->key = succ->key;
		node = succ;
	}
	
	free(node);
}

void Inorder (treeNodeType *tree_ptr)
{
	if (tree_ptr != NULL)
	{
		Inorder(tree_ptr->left);
		printf("노드의 값은 %d 입니다.\n", tree_ptr->key);
		Inorder(tree_ptr->right);
	}
}
```
`bstree.c`
```c
#include <stdio.h>
#include <stdlib.h>
#include "bstree.h"

void main()
{
	treeNodeType *n;
	initTree();
	
	root = insertBST(root, 40);
	insertBST(root, 18);
	insertBST(root, 55);
	insertBST(root, 10);
	insertBST(root, 25);
	insertBST(root, 45);
	insertBST(root, 75);
	
	Inorder(root);
	
	n = searchBST(root, 26);
	if (n == NULL) printf("헤당 키를 가진 노드가 없습니다.\n");
	else printf("데이터 %d를 찾았습니다.\n", n->key);
	
	deleteNode(root, 40);
	Inorder(root);
}
```
