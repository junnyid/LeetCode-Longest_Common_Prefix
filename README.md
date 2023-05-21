# LeetCode-Longest_Common_Prefix
**Longest Common Prefix**

Write a function to find the longest common prefix string amongst an array of strings.
If there is no common prefix, return an empty string "".
My approaches 
1. create size for strs
2. if size is 0, return empty strings
3. sort the array of string
4. find minimum length
5. find the common prefix

'''
class Solution:
    def longestCommonPrefix(self, strs: List[str]) -> str:
        size = len(strs)
        
        if (size == 0):
            return ""
        
        if (size == 1):
            return strs[0]
        
        strs.sort()
        end = min(len(strs[0]), len(strs[size - 1]))
        
        i = 0
        while (i < end and 
               strs[0][i] == strs[size - 1][i]):
            i += 1
            
        pre = strs[0][0: i]
        
        return pre
        '''
