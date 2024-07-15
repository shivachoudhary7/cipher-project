#include <iostream>
using namespace std;

struct TreeNode {
    int val;
    TreeNode *left;
    TreeNode *right;
    TreeNode(int x) : val(x), left(nullptr), right(nullptr) {}
};

class BST {
public:
    TreeNode* root;
    BST() : root(nullptr) {}

    // Function to insert a new node in the BST
    void insert(int key) {
        root = insertRec(root, key);
    }

    // Function to search a key in the BST
    bool search(int key) {
        return searchRec(root, key);
    }

private:
    // Helper function for insert
    TreeNode* insertRec(TreeNode* node, int key) {
        if (node == nullptr) {
            return new TreeNode(key);
        }
        if (key < node->val) {
            node->left = insertRec(node->left, key);
        } else if (key > node->val) {
            node->right = insertRec(node->right, key);
        }
        return node;
    }

    // Helper function for search
    bool searchRec(TreeNode* node, int key) {
        if (node == nullptr) {
            return false;
        }
        if (node->val == key) {
            return true;
        }
        if (key < node->val) {
            return searchRec(node->left, key);
        }
        return searchRec(node->right, key);
    }
};

int main() {
    BST tree;
    tree.insert(50);
    tree.insert(30);
    tree.insert(20);
    tree.insert(40);
    tree.insert(70);
    tree.insert(60);
    tree.insert(80);

    cout << "Search 40: " << (tree.search(40) ? "Found" : "Not Found") << endl;
    cout << "Search 25: " << (tree.search(25) ? "Found" : "Not Found") << endl;

    return 0;
}
