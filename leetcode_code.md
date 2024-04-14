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

# **[1119. Remove Vowels from a String](https://leetcode.com/problems/remove-vowels-from-a-string)**

```python
class Solution(object):
    def removeVowels(self, s):
        ret = ''
        for i in s:
            if i not in 'aeiou':
                ret += i
        return ret
```

# **[1119. Remove Vowels from a String](https://leetcode.com/problems/remove-vowels-from-a-string)**

```python
class Solution(object):
    def removeVowels(self, s):
        ret = ''
        for i in s:
            if i not in 'aeiou':
                ret += i
        return ret
```

# **[1108. Defanging an IP Address](https://leetcode.com/problems/defanging-an-ip-address)**

```python
class Solution(object):
    def defangIPaddr(self, address):
        ret = ''
        for i in address:
            if i != '.':
                ret += i
            else:
                ret += '[.]'
        return ret
```

# **[1689. Partitioning Into Minimum Number Of Deci-Binary Numbers](https://leetcode.com/problems/partitioning-into-minimum-number-of-deci-binary-numbers)**

```python
class Solution(object):
    def minPartitions(self, n):
        return int(max(n))
```

# **[771. Jewels and Stones](https://leetcode.com/problems/jewels-and-stones)**

```python
class Solution(object):
    def numJewelsInStones(self, jewels, stones):
        count = 0
        setJ = set(jewels)
        for i in setJ:
            count += stones.count(i)

        return count
```

# **[2942. Find Words Containing Character](https://leetcode.com/problems/find-words-containing-character)**

```python
class Solution(object):
    def findWordsContaining(self, words, x):
        ret = []
        for i in range(len(words)):
            if x in words[i]:
                ret.append(i)
        return ret
```

# **[1165. Single-Row Keyboard](https://leetcode.com/problems/single-row-keyboard)**

```python
class Solution(object):
    def calculateTime(self, keyboard, word):
        distance = 0
        currentIndex = 0
        key_map = {}

        for i, key in enumerate(keyboard):
            key_map[key] = i
        
        for letter in word:
            distance += abs(key_map[letter] - currentIndex)
            currentIndex = key_map[letter]

        return distance
```

# **[1678. Goal Parser Interpretation](https://leetcode.com/problems/goal-parser-interpretation/solutions/1769513/python-4-ways-to-attack/)**

```python
class Solution(object):
    def interpret(self, command):
        command = command.replace('()', 'o')
        command = command.replace('(al)', 'al')
        return command
```

# **[2114. Maximum Number of Words Found in Sentences](https://leetcode.com/problems/maximum-number-of-words-found-in-sentences)**

```python
class Solution(object):
    def mostWordsFound(self, sentences):
        maxWords = 0
        for sentence in sentences:
            wordsInSentence = sentence.count(' ') + 1
            maxWords = max(wordsInSentence, maxWords)
        
        return maxWords
```

# **[1221. Split a String in Balanced Strings](https://leetcode.com/problems/split-a-string-in-balanced-strings)**

```python
class Solution(object):
    def balancedStringSplit(self, s):
        balance = 0
        count = 0
        for i in s:
            balance += 1 if i == 'R' else -1
            if balance == 0:
                count += 1
        
        return count
```

# **[2125. Number of Laser Beams in a Bank](https://leetcode.com/problems/number-of-laser-beams-in-a-bank)**

```python
class Solution(object):
    def numberOfBeams(self, bank):
        beams = 0
        currentRow = 0
        nextRow = 0

        for i in bank:
            if nextRow == 0 and currentRow != 0:
                nextRow = i.count('1')
            if currentRow == 0:
                currentRow = i.count('1')
            if nextRow != 0 and currentRow != 0:
                beams += currentRow * nextRow
                currentRow = nextRow
                nextRow = 0
        return beams
```

# **[1769. Minimum Number of Operations to Move All Balls to Each Box](https://leetcode.com/problems/minimum-number-of-operations-to-move-all-balls-to-each-box)**

```python
class Solution(object):
    def minOperations(self, boxes):
        ans = [0]*len(boxes)
        leftCount, leftCost, rightCount, rightCost, n = 0, 0, 0, 0, len(boxes)
        for i in range(1, n):
            if boxes[i-1] == '1': leftCount += 1
            leftCost += leftCount # each step move to right, the cost increases by # of 1s on the left
            ans[i] = leftCost
        for i in range(n-2, -1, -1):
            if boxes[i+1] == '1': rightCount += 1
            rightCost += rightCount
            ans[i] += rightCost
        return ans
```

# **[1662. Check If Two String Arrays are Equivalent](https://leetcode.com/problems/check-if-two-string-arrays-are-equivalent)**

```python
class Solution(object):
    def arrayStringsAreEqual(self, word1, word2):
        word1 = ''.join(word1)
        word2 = ''.join(word2)
        return word1 == word2
```

# **[1920. Build Array from Permutation](https://leetcode.com/problems/build-array-from-permutation/)**

```python
class Solution(object):
    def buildArray(self, nums):
        ret = []

        for i in range(len(nums)):
            ret.append(nums[nums[i]])
        return ret
```
