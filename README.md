# DSA-POTD-questions-

vector<int> levelOrder(Node* root)
    {
      
        //Your code here
        
        vector<int> ans;
        queue<Node*> q;
        q.push(root);
        q.push(NULL);
            
            while(!q.empty())
            {
                Node* temp = q.front();
                q.pop();
            
                if(temp != NULL)
                {
                    ans.push_back(temp -> data);
                
                    if(temp ->left)
                    {
                        q.push(temp ->left);
                    }
        
                    if(temp ->right)
                    {
                        q.push(temp ->right);
                    }
                }
            }
        return ans;
    }
