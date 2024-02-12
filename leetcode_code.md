# **[1768. Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately)**

```python
class Solution(object):
    def mergeAlternately(self, word1, word2):
        merged = ''
        ranger = max(len(word1), len(word2))
        for x in range(ranger):
            if x < len(word1):
                merged += word1[x]
            if x < len(word2):
                merged += word2[x]
        return merged
```

# **[1071. Greatest Common Divisor of Strings](https://leetcode.com/problems/greatest-common-divisor-of-strings)**

```python
class Solution(object):
    def gcdOfStrings(self, str1, str2):
        if str1 + str2 != str2 + str1:
            return ''

        gcd = 1

        for i in range(1, min(len(str1), len(str2)) + 1):
            if len(str1) % i == 0 and len(str2) % i == 0:
                gcd = i
        
        return str1[0:gcd]
```

# **[1431. Kids With the Greatest Number of Candies](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies)**

```python
class Solution(object):
    def kidsWithCandies(self, candies, extraCandies):
        output = []
        maxCandies = 0
        for i in candies:
            if i > maxCandies:
                maxCandies = i
        
        for j in candies:
            output.append(True) if extraCandies + j >= maxCandies else output.append(False)
        
        return output
```

# **[605. Can Place Flowers](https://leetcode.com/problems/can-place-flowers)**

```python
    def canPlaceFlowers(self, flowerbed, n):
        if n == 0:
            return True
        for i in range(len(flowerbed)):
            if flowerbed[i] == 0 and (i == 0 or flowerbed[i-1] == 0) and (i == len(flowerbed)-1 or flowerbed[i+1] == 0):
                flowerbed[i] = 1
                n -= 1
                if n == 0:
                    return True
        return False
```

# **[345. Reverse Vowels of a String](https://leetcode.com/problems/reverse-vowels-of-a-string)**

```python
class Solution(object):
    def reverseVowels(self, s):
        s = list(s)
        a = 0
        b = len(s) - 1
        vowels = set('aeiouAEIOU')

        while a < b:
            if s[a] not in vowels:
                a += 1
            elif s[b] not in vowels:
                b -= 1
            else:
                s[a], s[b] = s[b], s[a]
                a += 1
                b -= 1
        
        return ''.join(s)
```

# **[151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string)**

```python
class Solution(object):
    def reverseWords(self, s):
        s = s.split()
        return ' '.join(reversed(s))
```
