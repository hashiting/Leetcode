> Q:Write a function to find the longest common prefix string amongst an array of strings.
> The solution is as below:

```C++
string longestCommonPrefix(vector<string>& strs) {
        string result = "";
        if(strs.size() == 0) return result;
        for(int i = 0;i < strs[0].size();i++){
            for(int j = 1;j < strs.size();j++){
                if(i>=strs[j].size()||strs[j][i] != strs[0][i]) return result;
            }
            result.push_back(strs[0][i]);
        }
        return result;
}
```
> The question asks about common prefix for all strings,so you can't just find the longest common prefix for two strings.
