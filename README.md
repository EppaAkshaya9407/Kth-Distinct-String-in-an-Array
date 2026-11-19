# Kth-Distinct-String-in-an-Array
class Solution:
    def kthDistinct(self, arr: list[str], k: int) -> str:
        count=Counter(arr)
        r=0
        for i,c in count.items():
            if c==1:
                r+=1
                if r==k:
                    return i
        return ""
