```sql
SELECT a.year AS '출시 연도', a.iphone, s.galaxy
FROM project.apple a
INNER JOIN project.samsung s 
ON a.year = s.year
ORDER BY a.year;
```
```sql
SELECT a.date AS 'Jan ~ Dec', a.iphone, s.galaxy
FROM project.apple a
INNER JOIN project.samsung s 
ON a.date = s.date;
```
```sql
SELECT a.year, COUNT(a.iphone) AS '연도별 애플 제품 출시 수'
FROM project.apple a
GROUP BY a.year
HAVING COUNT(*) > 1
```
```sql
SELECT s.year, COUNT(s.galaxy) AS '연도별 삼성 제품 출시 수'
FROM project.samsung s
GROUP BY s.year
HAVING COUNT(*) > 1
```
