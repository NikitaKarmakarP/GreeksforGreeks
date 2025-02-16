class Solution {
  public:
    // Function to serialize a tree and return a list containing nodes of tree.
    void inorder(Node* root,vector<int> &ans){
        if(!root) return ;
        
        inorder(root->left,ans);
        ans.push_back(root->data);
        inorder(root->right,ans);
    }
    vector<int> serialize(Node *root) {
         vector<int> ans ;
         inorder(root,ans);
         return ans;
    }

    // Function to deserialize a list and construct the tree.
    Node* contstruct(vector<int> &arr,int s,int e){
        if(s >e){
            return NULL;
        }
        int mid = (s+e)/2;
        Node* root = new Node(arr[mid]);
        root->left = contstruct(arr,s,mid-1);
        root->right = contstruct(arr,mid+1,e);
        return root;
    }
    Node *deSerialize(vector<int> &arr) {
         return contstruct(arr,0,arr.size()-1);
    }
};
