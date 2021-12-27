string longestPalin (string S)
{

        int n = S.length();
        
        string ans = "";
        
        for (int i = 0; i < n; i++)
        
        {
        
            int j = i;
            
            int k = i;
            
            while (j >= 0 && k < n && S[j] == S[k])
            
            {
            
                j--;
                
                k++;
                
            }
            
            if (k - j - 1 > ans.length())
            
                ans = S.substr(j + 1, k - j - 1);
                
        }
        for (int i = 0; i < n - 1; i++)
        {
        
            int j = i;
            
            int k = i + 1;
            
            while (j >= 0 && k < n && S[j] == S[k])
            {
            
                j--;
                
                k++;
                
            }
            
            if (k - j - 1 > ans.length())
            
                ans = S.substr(j + 1, k - j - 1);
                
        }
        
        return ans;
        
    }
