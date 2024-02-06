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

# **[Average Population](https://www.hackerrank.com/challenges/average-population/problem)**

**Solution**
```sql
SELECT ROUND(AVG(Population), 0) FROM City;
```

# **[Average Population](https://www.hackerrank.com/challenges/average-population/problem)**

**Solution**
```sql
SELECT ROUND(AVG(Population), 0) FROM City;
```

# **[Japan Population](https://www.hackerrank.com/challenges/japan-population/problem)**

**Solution**
```sql
SELECT SUM(Population) FROM City WHERE CountryCode = 'JPN';
```

# **[Population Density Difference](https://www.hackerrank.com/challenges/population-density-difference/problem)**

**Solution**
```sql
SELECT MAX(Population) - MIN(Population) FROM City;
```

# **[The Blunder](https://www.hackerrank.com/challenges/the-blunder/problem)**

**Solution**
```sql
SELECT CEIL(AVG(Salary) - AVG(Replace(Salary, 0, ''))) FROM Employees;
```

# **[Top Earners](https://www.hackerrank.com/challenges/earnings-of-employees/problem)**

**Solution**
```sql
SELECT months * salary AS earnings, COUNT(*)
FROM Employee
GROUP BY earnings
ORDER BY earnings desc
LIMIT 1;
```

# **[Weather Observation Station 2](https://www.hackerrank.com/challenges/weather-observation-station-2/problem)**

**Solution**
```sql
SELECT ROUND(SUM(LAT_N), 2), ROUND(SUM(LONG_W), 2) FROM Station;
```

# **[Weather Observation Station 13](https://www.hackerrank.com/challenges/weather-observation-station-13/problem)**

**Solution**
```sql
SELECT ROUND(SUM(LAT_N), 4) FROM Station WHERE LAT_N > 38.7880 AND LAT_N < 137.2345;
```

# **[Weather Observation Station 14](https://www.hackerrank.com/challenges/weather-observation-station-14/problem)**

**Solution**
```sql
SELECT ROUND(LAT_N, 4) FROM Station WHERE LAT_N < 137.2345 ORDER BY LAT_N DESC LIMIT 1; 
```

# **[Weather Observation Station 15](https://www.hackerrank.com/challenges/weather-observation-station-15/problem)**

**Solution**
```sql
SELECT ROUND(LONG_W, 4) FROM Station WHERE LAT_N < 137.2345 ORDER BY LAT_N DESC LIMIT 1;
```

# **[Weather Observation Station 16](https://www.hackerrank.com/challenges/weather-observation-station-16/problem)**

**Solution**
```sql
SELECT ROUND(LAT_N, 4) FROM Station WHERE LAT_N > 38.7780 ORDER BY LAT_N LIMIT 1;
```

# **[Weather Observation Station 17](https://www.hackerrank.com/challenges/weather-observation-station-17/problem)**

**Solution**
```sql
SELECT ROUND(LONG_W, 4) FROM Station WHERE LAT_N > 38.7780 ORDER BY LAT_N LIMIT 1;
```

# **[Weather Observation Station 18](https://www.hackerrank.com/challenges/weather-observation-station-18/problem)**

**Solution**
```sql
SELECT ROUND(ABS(MIN(LAT_N) - MAX(LAT_N)) + ABS(MIN(LONG_W) - MAX(LONG_W)), 4) FROM Station;
```

# **[Weather Observation Station 19](https://www.hackerrank.com/challenges/weather-observation-station-19/problem)**

**Solution**
```sql
select round(sqrt(power(max(LAT_N) - min(LAT_N), 2) + power(max(LONG_W) - min(LONG_W), 2)), 4) FROM STATION;
```

# **[Population Census](https://www.hackerrank.com/challenges/asian-population/problem)**

**Solution**
```sql
SELECT SUM(City.population)
FROM City
INNER JOIN Country
ON countrycode = code
WHERE continent = 'Asia';
```

# **[Average Population of Each Continent](https://www.hackerrank.com/challenges/average-population-of-each-continent/problem)**

**Solution**
```sql
SELECT continent, FLOOR(AVG(City.population)) AS average_population
FROM Country
INNER JOIN City
ON countrycode = code
GROUP BY continent
ORDER BY average_population;
```

# **[African Cities](https://www.hackerrank.com/challenges/african-cities/problem)**

**Solution**
```sql
SELECT City.name
FROM City
INNER JOIN Country
ON City.countrycode = Country.code
WHERE continent = 'Africa';
```
