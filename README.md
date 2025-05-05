# Day-19---SQL-learning-journal-


**Key Topics Covered:**
- **Mastering Multi-Table JOINs**
  - Successfully implemented **2- and 3-way JOINs** in real-world salary and player data from the #Moneyball database (CS50).
  - Key focus on bridging tables using appropriate keys (`player_id`, `team_id`, `id`).
- **Salary-Based Ranking**
  - Practiced **filtering salary data** with `WHERE`, `ORDER BY`, and `LIMIT`.
  - Filtered players and teams based on **salary thresholds**.
- **Real-World Data Application**
  - Used the `HAVING` clause to filter results after aggregation, ensuring insights are tailored to specific criteria.

**Skills Reinforced:**
- **SQL Aggregates:** Understanding of **SUM()**, **AVG()**, and **COUNT()** in relation to multi-table JOINs.
- **Logical Relationships:** Enhancing the ability to correctly **JOIN** related data from multiple tables while maintaining logical connections.

---SQL 

SELECT teams.name, AVG(salaries.salary) AS average_salary
FROM teams
JOIN salaries ON teams.id = salaries.team_id
WHERE salaries.year IN (1999, 2000, 2001)
GROUP BY teams.name
HAVING AVG(salaries.salary) > 2500000
ORDER BY average_salary DESC
LIMIT 10;

SELECT teams.name, salaries.year, AVG(salaries.salary) AS average_salary
FROM teams
JOIN salaries ON teams.id = salaries.team_id
WHERE salaries.year IN (1999, 2000, 2001)
GROUP BY teams.name, salaries.year
HAVING AVG(salaries.salary) > 2500000
ORDER BY salaries.year ASC, average_salary DESC
LIMIT 10;


**Next Focus:**
- Moving forward with more advanced queries, including **subqueries** and **advanced aggregation** using `HAVING` and `GROUP BY`.

**Badge Earned:**
- `SQL ADVANCED` – Taking another step towards a junior data engineering role.

---
