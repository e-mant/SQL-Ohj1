# OSIO 2: Relaatiotietokannan peruskäsitteiden harjoitukset

### Tehtävä 1

vastaus: 5

### Tehtävä 2

vastaus: 5

### Tehtävä 3

vastaus: ident

### Tehtävä 4

vastaus: varchar

### Tehtävä 5

vastaus: iso_country

### Tehtävä 6

vastaus: country

### Tehtävä 7

vastaus: iso_country

### Tehtävä 8

vastaus: varchar

### Tehtävä 9

vastaus: 70942

### Tehtävä 10

vastaus: iso_country

### Tehtävä 11

vastaus: varchar

### Tehtävä 12

vastaus: 248

### Tehtävä 13

vastaus: goal

### Tehtävä 14

vastaus: 0DEG

### Tehtävä 15

vastaus: id

### Tehtävä 16

vastaus: Epätosi

### Tehtävä 17

vastaus: game

### Tehtävä 18

vastaus: game

### Tehtävä 19

vastaus: game

### Tehtävä 20

vastaus: game

### Tehtävä 21

vastaus: id

### Tehtävä 22

vastaus: location

### Tehtävä 23

vastaus: goal_reached

### Tehtävä 24

vastaus: goal_id, game_id

### Tehtävä 25

vastaus: 2

# OSIO 3: Yhteen tauluun kohdistuvien kyselyiden harjoitukset

### Tehtävä 1

select * from goal;

![image](https://github.com/user-attachments/assets/e16cab4b-301e-4b88-ba21-dcfe198920ce)

### Tehtävä 2

select name from airport where iso_country = "FI";

![image](https://github.com/user-attachments/assets/e0e93c1e-1861-4bde-8d3f-baf76e0c211c)

### Tehtävä 3

select name from airport where iso_country = "FI" order by name asc;

![image](https://github.com/user-attachments/assets/e5fa289d-5325-4e8d-a9e0-53e04bb62174)

### Tehtävä 4

select name, type from airport where iso_country = "FI" order by type asc, name asc;

![image](https://github.com/user-attachments/assets/a1763a83-b15c-4734-aa5d-5642de9c4fb8)

### Tehtävä 5

select name from country where name like "f%";

![image](https://github.com/user-attachments/assets/e752f936-0b8d-424a-9c72-a15f11c79531)

### Tehtävä 6

select name from country where name like "%f%";

![image](https://github.com/user-attachments/assets/5615a8e1-1b38-470b-9e4b-4330abe55392)

### Tehtävä 7

select location from game where screen_name = "Vesa";

![image](https://github.com/user-attachments/assets/ec9ebffb-0055-4b81-b408-e463ae5a96d9)

### Tehtävä 8

select co2_consumed from game where screen_name = "Ilkka";

![image](https://github.com/user-attachments/assets/8f8590e8-9f02-4768-8374-edaa5167bbb2)

### Tehtävä 9

select distinct co2_budget from game;

![image](https://github.com/user-attachments/assets/4be1f833-afdf-43ef-ad7d-ad7106f7711d)

# OSIO 4: Where-osan liitosehto harjoitukset

### Tehtävä 1

select country.name as "country name", airport.name as "airport name" from airport, country where airport.iso_country = country.iso_country and country.name = "Iceland";

![image](https://github.com/user-attachments/assets/87f91d46-8ad5-4a45-9e31-6609ec57dc7e)

### Tehtävä 2

select airport.name as "airport name" from airport, country where airport.iso_country = country.iso_country and country.name = "France" and airport.type = "large_airport";

![image](https://github.com/user-attachments/assets/80ba5b04-7d76-4ba6-ae00-db9790eb70dd)

### Tehtävä 3

select country.name as country_name, airport.name as airport_name from airport, country where airport.iso_country = country.iso_country and country.continent = "AN";

![image](https://github.com/user-attachments/assets/552f1635-b146-4113-be3a-f6fac86265e3)

### Tehtävä 4

select elevation_ft from airport, game where location = ident and screen_name = "Heini";

![image](https://github.com/user-attachments/assets/4b5f90b1-bec4-4e7f-bed9-52248cd81390)

### Tehtävä 5

select elevation_ft * 0.3048 as elevation_m from airport, game where location = ident and screen_name = "Heini";

![image](https://github.com/user-attachments/assets/8eae1858-f8a1-4847-bbd7-58f38f37b599)

### Tehtävä 6

select name from airport, game where location = ident and screen_name = "Ilkka";

![image](https://github.com/user-attachments/assets/30af2622-a3b0-4f5a-baf2-71ad4638dc36)

### Tehtävä 7

select country.name from airport, game, country where location = ident and airport.iso_country = country.iso_country  and screen_name = "Ilkka";

![image](https://github.com/user-attachments/assets/2852d10a-8ae4-4146-a8db-536bd1bd97e2)

### Tehtävä 8

select name from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini";

![image](https://github.com/user-attachments/assets/21d0d5d8-95f1-4710-8557-e46435cf3099)

### Tehtävä 9

select airport.name from airport, game, goal, goal_reached where ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";

![image](https://github.com/user-attachments/assets/4a5db197-2ecb-4b76-b8b6-ff1d2246b260)

### Tehtävä 10

select country.name from country, airport, game, goal, goal_reached where airport.iso_country = country.iso_country and ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";

![image](https://github.com/user-attachments/assets/c8055cc0-c5bd-4cd0-bace-375610c08101)



