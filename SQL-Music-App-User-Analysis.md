SQL Mini-Project: Music App User Analysis

1. Project Objective
Use SQL to analyze a sample dataset of music app users and answer basic questions about their listening activity.
2. Dataset
Table name: users

| user_id | name | country | weekly_minutes |
|---|---|---|---|
| 1 | Asha | India | 180 |
| 2 | Rahul | India | 75 |
| 3 | Mia | UK | 240 |
| 4 | John | US | 110 |
| 5 | Sara | UK | 60 |
| 6 | Arjun | India | 210 |

Column descriptions:
user_id: Unique identifier for each user.
name: Name of the user.
country: Country of the user.
weekly_minutes: Number of minutes the user listened to music in one week.

## 3. SQL Queries

### Query 1: Display All Users

**Question:** How can we display all columns for every user?

```sql
SELECT *
FROM users;
```

**Description:** Retrieves all columns and rows from the `users` table.

---

### Query 2: Display User Names and Countries

**Question:** How can we display only the name and country of each user?

```sql
SELECT name, country
FROM users;
```

**Description:** Retrieves only the `name` and `country` columns.

---

### Query 3: Find Users from India

**Question:** Which users are from India?

```sql
SELECT *
FROM users
WHERE country = 'India';
```

**Description:** Displays users whose country is India.

---

### Query 4: Find Users Who Listened for More Than 100 Minutes

**Question:** Which users listened for more than 100 minutes per week?

```sql
SELECT *
FROM users
WHERE weekly_minutes > 100;
```

**Description:** Displays users whose weekly listening time exceeds 100 minutes.

---

### Query 5: Find Indian Users Who Listened for More Than 100 Minutes

**Question:** Which users are from India and listened for more than 100 minutes per week?

```sql
SELECT *
FROM users
WHERE country = 'India'
  AND weekly_minutes > 100;
```

**Description:** Displays users who meet both conditions.

---

### Query 6: Find the Top Three Users by Listening Time

**Question:** Who are the three users with the highest weekly listening time?

```sql
SELECT name, weekly_minutes
FROM users
ORDER BY weekly_minutes DESC
LIMIT 3;
```

**Description:** Sorts users by weekly listening time from highest to lowest and returns the top three.

4. Conclusion
   
These  SQL queries demonstrate how to retrieve, filter, and sort data from a table of music app users.
The queries use SELECT, FROM, WHERE, AND, ORDER BY, and LIMIT to answer basic questions about user behaviour.

Dataset note: This project uses fictional sample data for learning purposes.




