SELECT
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

BASIC JOINS
==============

# **[1581. Customer Who Visited but Did Not Make Any Transactions](https://leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions/)**

**Solution**
```sql
select customer_id, count(customer_id) as count_no_trans
from Visits
where visit_id not in (
    select visit_id 
    from transactions
    )
group by customer_id;

select customer_id, count(customer_id) as count_no_trans
from Visits as v
left join Transactions as t
on v.visit_id = t.visit_id
where transaction_id is null
group by customer_id;
```

# **[175. Combine Two Tables](https://leetcode.com/problems/combine-two-tables/solutions/)**

**Solution**
```sql
select firstName, lastName, city, state
from Person p
left join Address a
on p.personId = a.personId;
```

# **[175. Combine Two Tables](https://leetcode.com/problems/combine-two-tables/)**

**Solution**
```sql
select user_id as buyer_id, join_date, count(order_date) as orders_in_2019
from Users u
left join Orders o
on u.user_id = o.buyer_id
and year(order_date) = 2019
group by user_id;
```

# **[175. Combine Two Tables](https://leetcode.com/problems/combine-two-tables/)**

**Solution**
```sql
select user_id as buyer_id, join_date, count(order_date) as orders_in_2019
from Users u
left join Orders o
on u.user_id = o.buyer_id
and year(order_date) = 2019
group by user_id;
```
