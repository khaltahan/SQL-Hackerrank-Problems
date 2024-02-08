# **[the PADS](https://www.hackerrank.com/challenges/the-pads/problem)**

**Solution**
```sql
SELECT CONCAT(name, '(', SUBSTRING(occupation, 1, 1), ')')
FROM Occupations
ORDER BY name;

SELECT CONCAT('There are a total of ', COUNT(occupation), ' ', LOWER(occupation) ,'s.')
FROM Occupations
GROUP BY occupation
ORDER BY COUNT(occupation), occupation;
```

# **[Occupations](https://www.hackerrank.com/challenges/occupations/problem)**

**Solution**
```sql
SELECT CONCAT(name, '(', SUBSTRING(occupation, 1, 1), ')')
FROM Occupations
ORDER BY name;

SELECT CONCAT('There are a total of ', COUNT(occupation), ' ', LOWER(occupation) ,'s.')
FROM Occupations
GROUP BY occupation
ORDER BY COUNT(occupation), occupation;
```
