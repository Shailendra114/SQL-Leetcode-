# SQL-Leetcode-Questions-Collection

This repo contains all my SQL solutions from Leetcode website in order to practice SQL programming skills. I attempted all questions in 25 days to corroborate my knowledge in SQL.

### Description

The solutions are divided into three level of categories namely Easy, Medium, and Hard. Every category first contains the question and then followed by its respective solution. Link to the website is:-

https://leetcode.com/problemset/database/
 
**Question  01**

**Table: ActorDirector**   

| Column Name | Type |
|-------------|------|
| actor_id    | int  |
| director_id | int  |
| timestamp   | int  |



-- timestamp is the primary key column for this table.
 

-- Write a SQL query for a report that provides the pairs (actor_id, director_id) where the actor have cooperated with the director at least 3 times.

-- Example:

**ActorDirector table**


             
   | actor_id    | director_id | timestamp   |             
   |-------------|-------------|-------------|
   | 1           | 1           | 0           |
   | 1           | 1           | 1           |
   | 1           | 1           | 2           |
   | 1           | 2           | 3           |
   | 1           | 2           | 4           |
   | 2           | 1           | 5           |
   | 2           | 1           | 6           |
  


--   Result table:


   | actor_id    | director_id |
   |-------------|-------------|
   | 1           | 1           |
   


--  The only pair is (1, 1) where they cooperated exactly 3 times.

-- Solution 
``` sql
Select actor_id, director_id
from actordirector
group by actor_id, director_id
having count(*)>=3






