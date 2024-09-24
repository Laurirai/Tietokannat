# Viikko 3 tehtävät

# Teht1

SELECT * FROM taulu WHERE kentta = 'arvo'

![kuvankaappaus](ScreenShot1.png)

# Teht2

SELECT * FROM taulu WHERE kentta = 'arvo' WHERE joku = 4

![kuvankaappaus](ScreenShot2.png)

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