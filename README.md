# remove-common-chars

class Solution
{
    public:
    //Function to remove common characters and concatenate two strings.
    string concatenatedString(string s1, string s2) 
    { 
        // Your code here
        unordered_set<char>st,set;
        for(int i=0;i<s1.size();i++){
            st.insert(s1[i]);
        }
        for(int i=0;i<s2.size();i++){
            if(st.find(s2[i])!=st.end()){
                set.insert(s2[i]);
            }
        }
        string s=s1+s2;
        string ans="";
        for(int i=0;i<s.size();i++){
            if(set.find(s[i])==set.end()){
                ans+=s[i];
            }
        }
       if(ans.size()>0){
           return ans;
       }
       else{
           return "-1";
       }
    }
    

};
