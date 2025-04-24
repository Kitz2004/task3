# 📁 Anime Table Export

This repository contains the exported `anime` table from the MySQL database `folder1`. It includes the SQL file task3 for importing the table, along with documentation and example queries.

## 📦 Files Included

- `task3` – Full SQL dump of the `anime` table (structure + data)
- `README.md` – Project overview and usage instructions

## 📋 Table Overview

The `anime` table stores data about various anime series. It includes information such as the title, genre, number of episodes, rating, and release year.

-- 1. Get all anime entries
SELECT * FROM anime;

-- 2. Find top-rated anime (rating > 8)
SELECT * FROM anime WHERE rating > 8;

-- 3. Get anime released after 2020
SELECT * FROM anime WHERE release_year > 2020;

-- 4. Count anime by genre
SELECT genre, COUNT(*) AS total FROM anime GROUP BY genre;

-- 5. Average rating by release year
SELECT release_year, AVG(rating) AS avg_rating 
FROM anime 
GROUP BY release_year 
ORDER BY release_year;
