```python

class Solution(object):
    def lengthOfLongestSubstring(self, s):
        """
        :type s: str
        :rtype: int
        """
        str = ''
        longest = ''
        for i in s:
            if i not in str:
                str += i
            else:
                if len(str) > len(longest):
                    longest = str
                str = str[str.index(i) + 1:] + i
        if len(str) > len(longest): 
            longest = str
        return len(longest)     
        
