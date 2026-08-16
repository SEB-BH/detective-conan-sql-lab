<h1>
  <span class="headline">The Moonlit Pearl Case</span>
  <span class="subhead">Instructor Guide</span>
</h1>

## Overview

This is a drop-in alternative to the Carmen Sandiego Intro to SQL lab. It keeps the original seven-clue structure and the same core SQL commands while using a smaller GCC-centered database and a Detective Conan story.

The mystery is designed for approximately 90 minutes of independent or pair work.

## SQL coverage

| Clue | Main SQL practice |
| ---- | ----------------- |
| 1 | `SELECT`, `FROM`, `WHERE`, `ORDER BY`, `LIMIT` |
| 2 | `WHERE`, `AND`, Boolean comparison |
| 3 | table aliases, `JOIN`, `ON`, multiple `AND` conditions |
| 4 | `<>` comparison |
| 5 | `JOIN`, `ON`, and `LIKE` pattern matching |
| 6 | joining a country's `capital_id` to a city's `id` |
| 7 | numeric equality in a `WHERE` clause |

## Answer path

1. Bahrain (`BHR`)
2. Arabic
3. Oman (`OMN`)
4. Sohar
5. Sharjah, United Arab Emirates (`ARE`)
6. Abu Dhabi
7. Doha, Qatar

The final answer is **Doha**.

## Suggested facilitation

- Ask students to begin with `SELECT * FROM table_name;` when they are unsure what a table contains.
- Encourage them to solve and run one clue at a time rather than writing all seven queries before testing.
- For Clue 3, remind students that the requested evidence is split between `countries` and `official_languages`.
- For Clue 5, ask which wildcard can represent the missing letters after `Sh`.
- For Clue 6, draw attention to the fact that `capital_id` stores a city ID, not a city name.
- Avoid giving students the country codes in advance. Each result supplies the code needed for the next query.

## Verify the solution

From the package directory:

```bash
cd detective-conan-sql-lab-starter-code
psql -f case_database.sql
psql -d conan_case -f ../detective-conan-sql-lab-solution/solution.sql
```

Each query should return a single intended result.

## Data note

This is intentionally a compact case database, not a complete geography database. Population figures are simplified values created for the mystery and should not be presented as current statistics.
