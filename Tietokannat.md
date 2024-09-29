# Viikko 1 Relaatiotietokannan peruskäsitteiden harjoitukset

![kuvankaappaus](eka_viikko_kaikki_tehty.png)

# Viikko2

### Teht 1

SELECT id, name, description, icon, target, target_minvalue, target_maxvalue, target_text FROM goal;

![kuvankaappaus](Vk2T1.png)

### Teht 2

SELECT name, type FROM airport WHERE iso_country = 'FI';

![kuvankaappaus](Vk2T2.png)

### Teht 3

SELECT name FROM airport WHERE iso_country = 'FI' ORDER BY name ASC;

![kuvankaappaus](Vk2T3.png)

### Teht 4

SELECT name, type FROM airport WHERE iso_country = 'FI' ORDER BY type, name;

![kuvankaappaus](Vk2T4.png)

### Teht 5

SELECT name FROM country WHERE name LIKE 'F%';

![kuvankaappaus](Vk2T5.png)

### Teht 6

SELECT name FROM country WHERE name LIKE '%F%';

![kuvankaappaus](Vk2T6.png)

### Teht 7

SELECT location FROm game WHERE screen_name = 'Vesa';

![kuvankaappaus](Vk2T7.png)

### Teht 8

SELECT co2_consumed FROM game WHERE screen_name = 'Ilkka';

![kuvankaappaus](Vk2T8.png)

### Teht 9

SELECT co2_budget FROM game LIMIT 1;

![kuvankaappaus](Vk2T9.png)

# Viikko 2 Where tehtävät

### Teht 1

SELECT
    ->     CASE
    ->         WHEN iso_country = "IS" THEN "Iceland"
    ->         ELSE iso_country
    ->     END AS "country name",
    ->     name AS "airport name"
    -> FROM airport
    -> WHERE iso_country = "IS";

![kuvankaappaus](Vk2where1.png)

### Teht 2

SELECT name AS "airport name" FROM airport WHERE iso_country = "FR" AND type = "large_airport";

![kuvankaappaus](Vk2where2.png)

### Teht 3

select country.name as "country_name", airport.name as "airport_name"
from airport, country
where country.continent like 'AN' AND airport.iso_country like country.iso_country

![kuvankaappaus](Vk2where3.png)

### Teht 4

SELECT elevation_ft FROM airport, game WHERE game.screen_name like 'Heini' and game.location like airport.ident;

![kuvankaappaus](Vk2where4.png)

### Teht 5

SELECT (elevation_ft * 0.3048) AS elevation_m FROM airport, game WHERE game.screen_name LIKE 'Heini' AND game.location LIKE airport.ident;

![kuvankaappaus](Vk2where5.png)

### Teht 6

SELECT name FROM airport, game WHERE game.screen_name LIKE 'Ilkka' AND game.location LIKE airport.ident
;

![kuvankaappaus](Vk2where6.png)

### Teht 7

SELECT c.name
    -> FROM game g
    -> JOIN airport a ON g.location = a.ident
    -> JOIN country c ON a.iso_country = c.iso_country
    -> WHERE g.screen_name = 'Ilkka';

![kuvankaappaus](Vk2where7.png)

### Teht 8

SELECT name FROM goal, goal_reached, game WHERE game.screen_name LIKE 'heini' AND game.id = game_id and goal.id=goal_id;

![kuvankaappaus](Vk2where8.png)

### Teht 9

SELECT airport.name FROM airport, game, goal, goal_reached WHERE game.screen_name LIKE 'Ilkka'
AND game.id = goal_reached.game_id AND goal.name LIKE 'CLOUDS' 
AND goal_reached.goal_id = goal.id AND game.location = airport.ident;

![kuvankaappaus](Vk2where9.png)

### Teht 10

select country.name
    ->      from country, goal, goal_reached, airport, game
    ->     where game.screen_name = "Ilkka" AND goal.name = 'CLOUDS' AND game.id = goal_reached.game_id and goal_reached.goal_id = goal.id and game.location = airport.ident AND airport.iso_country = country.iso_country;

![kuvankaappaus](Vk2where10.png)

# Viikko 3

### JOIN Teht 1

