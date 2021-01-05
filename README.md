1: SELECT COUNT(CountryCode)
   FROM city
   WHERE CountryCode= 'USA';

2: SELECT LifeExpectancy, Population 
   FROM country
   WHERE name= 'Argentina';

3: SELECT MAX(LifeExpectancy)
   FROM country;

4: SELECT city.name 
   FROM country  
   JOIN city ON country.capital = city.id 
   WHERE country.code = 'ESP';

6: SELECT name
   FROM city
   WHERE name like'F%' LIMIT 25; 

8: SELECT name, population 
   FROM country 
   WHERE population is not null limit 1;

9: SELECT count(name)
   FROM country;

10: SELECT name 

13: SELECT name, population/surfacearea as ratio
from country
where (population/surfacearea)> order by ratio 
limit 10;



16: SELECT name, count(language) as language_count
    FROM country
    JOIN countrylanguage on country.code = countrylanguage.countrycode
    GROUP BY name
    ORDER BY language_count DESC
    limit 10;

17: SELECT name from country 
JOIN countrylanguage on country.code= countrylanguage.countrycode
WHERE countrylanguage.language= 'german'and countrylanguage.percentage > 50;


19: SELECT governmentform, count(governmentform) 
    FROM country 
    GROUP BY governmentform
    ORDER BY count(governmentform) DESC
    limit 3;
