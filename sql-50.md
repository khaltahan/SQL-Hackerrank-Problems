SELECT QUESTIONS
==============

# **[1757. Recyclable and Low Fat Products](https://leetcode.com/problems/recyclable-and-low-fat-products)**

**Solution**
```sql
select product_id from Products where low_fats = 'Y' and recyclable = 'Y';
```

# **[584. Find Customer Referee](https://leetcode.com/problems/find-customer-referee)**

**Solution**
```sql
select product_id from Products where low_fats = 'Y' and recyclable = 'Y';
```

# **[595. Big Countries](https://leetcode.com/problems/big-countries)**

**Solution**
```sql
select name, population, area from World where population >= 25000000 or area >= 3000000;
```

# **[1148. Article Views I](https://leetcode.com/problems/article-views-i)**

**Solution**
```sql
select distinct author_id as id from Views where author_id = viewer_id order by id;
```

# **[1683. Invalid Tweets](https://leetcode.com/problems/invalid-tweets)**

**Solution**
```sql
select tweet_id from Tweets where length(content) > 15;
```
