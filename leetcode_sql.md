# **[1757. Recyclable and Low Fat Products](https://leetcode.com/problems/recyclable-and-low-fat-products)**

```sql
select product_id from Products where low_fats = 'Y' and recyclable = 'Y';
```

# **[584. Find Customer Referee](https://leetcode.com/problems/find-customer-referee)**

```sql
select product_id from Products where low_fats = 'Y' and recyclable = 'Y';
```

# **[595. Big Countries](https://leetcode.com/problems/big-countries)**

```sql
select name, population, area from World where population >= 25000000 or area >= 3000000;
```

# **[1148. Article Views I](https://leetcode.com/problems/article-views-i)**

```sql
select distinct author_id as id from Views where author_id = viewer_id order by id;
```

# **[1683. Invalid Tweets](https://leetcode.com/problems/invalid-tweets)**

```sql
select tweet_id from Tweets where length(content) > 15;
```

# **[1581. Customer Who Visited but Did Not Make Any Transactions](https://leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions/)**

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

```sql
select firstName, lastName, city, state
from Person p
left join Address a
on p.personId = a.personId;
```

# **[1158. Market Analysis I](https://leetcode.com/problems/market-analysis-i/)**

```sql
select user_id as buyer_id, join_date, count(order_date) as orders_in_2019
from Users u
left join Orders o
on u.user_id = o.buyer_id
and year(order_date) = 2019
group by user_id;
```

# **[607. Sales Person](https://leetcode.com/problems/sales-person)**

```sql
select name from salesperson
where sales_id not in 
(
    select sales_id from orders where com_id in 
	(select com_id from company where name='RED')
)

select name from salesperson
where sales_id not in
(select sales_id from orders
left join
company 
on orders.com_id=company.com_id 
where company.name='RED')
```

# **[183. Customers Who Never Order](https://leetcode.com/problems/customers-who-never-order/)**

```sql
select name as Customers from Customers where id not in (select customerId from Orders);

select name as Customers
from Customers c
left join Orders o
on c.id = o.customerId
where o.id is null;
```

# **[586. Customer Placing the Largest Number of Orders](https://leetcode.com/problems/customer-placing-the-largest-number-of-orders/)**

```sql
select customer_number
from Orders
group by customer_number
order by count(customer_number) desc
limit 1;

-- Follow up: What if more than one customer has the largest number of orders, can you find all the customer_number in this case?

select customer_number
from Orders
group by customer_number
having count(customer_number) = (
    select max(order_count)
    from (
        select count(customer_number) as order_count
        from Orders
        group by customer_number
    ) as temp
);
```

# **[1068. Product Sales Analysis I](https://leetcode.com/problems/product-sales-analysis-i)**

```sql
select product_name, year, price
from Product p
right join Sales s
on p.product_id = s.product_id;
```

# **[197. Rising Temperature](https://leetcode.com/problems/rising-temperature)**

```sql
select w1.id as Id
from Weather w1
join Weather w2
on datediff(w1.recordDate, w2.recordDate) = 1
where w1.temperature > w2.temperature;
```

# **[1661. Average Time of Process per Machine](https://leetcode.com/problems/average-time-of-process-per-machine)**

```sql
select a1.machine_id, round(avg(a2.timestamp - a1.timestamp), 3) as processing_time
from Activity a1
join Activity a2
on a1.machine_id = a2.machine_id 
    and a1.process_id = a2.process_id 
    and a2.activity_type = 'end'
    and a1.activity_type = 'start'
group by a1.machine_id;
```

# **[577. Employee Bonus](https://leetcode.com/problems/employee-bonus)**

```sql
select name, bonus
from Employee e
left join Bonus b
on e.empId = b.empId
where bonus < 1000 or bonus is null;
```

# **[1407. Top Travellers](https://leetcode.com/problems/top-travellers)**

```sql
select name, ifnull(sum(distance), 0) as travelled_distance
from Users u
left join Rides r
on u.id = r.user_id
group by u.id
order by travelled_distance desc, name;
```
