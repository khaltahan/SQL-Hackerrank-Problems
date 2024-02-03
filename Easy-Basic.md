# **[Revising the Select Query I](https://www.hackerrank.com/challenges/revising-the-select-query)**

**Solution**
```sql
SELECT * FROM City WHERE CountryCode = 'USA' AND Population > 100000;
```

# **[Revising the Select Query II](https://www.hackerrank.com/challenges/revising-the-select-query-2)**

**Solution**
```sql
SELECT Name FROM City WHERE CountryCode = 'USA' AND Population > 120000;
```

# **[Select All](https://www.hackerrank.com/challenges/select-all-sql)**

**Solution**
```sql
SELECT * FROM City;
```

# **[Select by ID](https://www.hackerrank.com/challenges/select-by-id)**

**Solution**
```sql
SELECT * FROM City WHERE id = 1661;
```

# **[Japanese Cities' Attributes](https://www.hackerrank.com/challenges/japanese-cities-detail)**

**Solution**
```sql
SELECT * FROM City WHERE CountryCode = 'JPN';      
```

# **[Japanese Cities' Names](https://www.hackerrank.com/challenges/japanese-cities-name)**

**Solution**
```sql
SELECT Name FROM City WHERE CountryCode = 'JPN';    
```

# **[Weather Observation Station 1](https://www.hackerrank.com/challenges/weather-observation-station-1)**

**Solution**
```sql
SELECT City, State FROM Station;   
```

# **[Weather Observation Station 3](https://www.hackerrank.com/challenges/weather-observation-station-3)**

**Solution**
```sql
SELECT DISTINCT City FROM Station WHERE MOD(id,2) = 0;     
```

# **[Weather Observation Station 4](https://www.hackerrank.com/challenges/weather-observation-station-4)**

**Solution**
```sql
SELECT COUNT(City) - COUNT(DISTINCT City) FROM Station;
```

# **[Weather Observation Station 5](https://www.hackerrank.com/challenges/weather-observation-station-5)**

**Solution**
```sql
SELECT City, LENGTH(City) FROM Station ORDER BY LENGTH(City), City LIMIT 1;
SELECT City, LENGTH(City) FROM Station ORDER BY LENGTH(City) DESC, City LIMIT 1;
```

# **[Weather Observation Station 6](https://www.hackerrank.com/challenges/weather-observation-station-6)**

**Solution**
```sql
SELECT DISTINCT City FROM Station WHERE UPPER(SUBSTRING(City, 1, 1)) IN ('A', 'E', 'I', 'O', 'U');
```

# **[Weather Observation Station 7](https://www.hackerrank.com/challenges/weather-observation-station-7)**

**Solution**
```sql
SELECT DISTINCT City FROM Station WHERE UPPER(SUBSTRING(City, length(City), 1)) IN ('A', 'E', 'I', 'O', 'U');
```

# **[Weather Observation Station 8](https://www.hackerrank.com/challenges/weather-observation-station-8/problem)**

**Solution**
```sql
SELECT City 
FROM Station 
WHERE UPPER(SUBSTRING(City, 1, 1)) IN ('A', 'E', 'I', 'O', 'U')
  AND UPPER(SUBSTRING(City, LENGTH(City), 1)) IN ('A', 'E', 'I', 'O', 'U');
```

# **[Weather Observation Station 9](https://www.hackerrank.com/challenges/weather-observation-station-9/problem)**

**Solution**
```sql
SELECT DISTINCT CITY FROM STATION WHERE UPPER(SUBSTRING(CITY, 1, 1)) NOT IN ('A', 'E', 'I', 'O', 'U');    
```

# **[Weather Observation Station 10](https://www.hackerrank.com/challenges/weather-observation-station-10/problem)**

**Solution**
```sql
SELECT DISTINCT CITY FROM STATION WHERE UPPER(SUBSTRING(CITY, LENGTH(City), 1)) NOT IN ('A', 'E', 'I', 'O', 'U');   
```

# **[Weather Observation Station 11](https://www.hackerrank.com/challenges/weather-observation-station-11/problem)**

**Solution**
```sql
SELECT DISTINCT City 
FROM Station 
WHERE UPPER(SUBSTRING(City, 1, 1)) NOT IN ('A', 'E', 'I', 'O', 'U')
   OR UPPER(SUBSTRING(City, LENGTH(City), 1)) NOT IN ('A', 'E', 'I', 'O', 'U');
```

# **[Weather Observation Station 12](https://www.hackerrank.com/challenges/weather-observation-station-12/problem)**

**Solution**
```sql
SELECT DISTINCT City 
FROM Station 
WHERE UPPER(SUBSTRING(City, 1, 1)) NOT IN ('A', 'E', 'I', 'O', 'U')
  AND UPPER(SUBSTRING(City, LENGTH(City), 1)) NOT IN ('A', 'E', 'I', 'O', 'U');
```

# **[Higher Than 75 Marks](https://www.hackerrank.com/challenges/more-than-75-marks/problem)**

**Solution**
```sql
SELECT name FROM Students WHERE marks > 75 ORDER BY SUBSTRING(name, LENGTH(name) - 2, 3), id;  
```

# **[Employee Names](https://www.hackerrank.com/challenges/name-of-employees/problem)**

**Solution**
```sql
SELECT name FROM Employee ORDER BY name;
```
# **[Employee Salaries](https://www.hackerrank.com/challenges/salary-of-employees/problem)**

**Solution**
```sql
SELECT name FROM Employee WHERE salary > 2000 AND months < 10 ORDER BY employee_id;
```

# **[Type of Triangle](https://www.hackerrank.com/challenges/what-type-of-triangle/problem)**

**Solution**
```sql
SELECT 
CASE
    WHEN (A + B <= C OR B + C <= A OR A + C <= B) THEN 'Not A Triangle'
    WHEN (A = B AND B = C) THEN 'Equilateral'
    WHEN (A = B OR B = C or A = C) THEN 'Isosceles'
    ELSE 'Scalene'
END
From Triangles;
```

# **[Revising Aggregations - The Count Function](https://www.hackerrank.com/challenges/revising-aggregations-the-count-function/problem)**

**Solution**
```sql
SELECT COUNT(DISTINCT Name) FROM City WHERE Population > 100000;
```

# **[Revising Aggregations - The Sum Function](https://www.hackerrank.com/challenges/revising-aggregations-sum/problem)**

**Solution**
```sql
SELECT SUM(Population) FROM City WHERE District = 'California';
```

# **[Revising Aggregations - The Avg Function](https://www.hackerrank.com/challenges/revising-aggregations-the-average-function/problem)**

**Solution**
```sql
SELECT AVG(Population) FROM City WHERE District = 'California';
```

# **[Average Population](https://www.hackerrank.com/challenges/average-population/problem)**

**Solution**
```sql
SELECT ROUND(AVG(Population), 0) FROM City;
```
