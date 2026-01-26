# Joins

---

| Join Type                  | Syntax                                         | Returns                                                         | NULL Behavior                                      | Use Case                                                             |
| -------------------------- | ---------------------------------------------- | --------------------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------------------------- |
| `INNER JOIN`               | `FROM A INNER JOIN B ON A.id = B.id`           | Only matching rows from both tables                             | Excludes rows where join condition is NULL         | Default choice; get related data that exists in both tables          |
| `LEFT JOIN` (LEFT OUTER)   | `FROM A LEFT JOIN B ON A.id = B.id`            | All rows from left table (A), matched rows from right table (B) | Returns NULLs for B columns when no match          | Keep all records from main table, show related data if exists        |
| `RIGHT JOIN` (RIGHT OUTER) | `FROM A RIGHT JOIN B ON A.id = B.id`           | All rows from right table (B), matched rows from left table (A) | Returns NULLs for A columns when no match          | Less common; usually rewritten as LEFT JOIN                          |
| `FULL OUTER JOIN`          | `FROM A FULL OUTER JOIN B ON A.id = B.id`      | All rows from both tables                                       | Returns NULLs where no match exists on either side | Find all records whether they match or not                           |
| `CROSS JOIN`               | `FROM A CROSS JOIN B` (or `FROM A, B`)         | Cartesian product (every row in A × every row in B)             | N/A (no join condition)                            | Generate all combinations; useful for creating test data or matrices |
| `SELF JOIN`                | `FROM A t1 JOIN A t2 ON t1.manager_id = t2.id` | Joins table to itself using aliases                             | Same as INNER/LEFT JOIN                            | Compare rows within same table (hierarchies, sequences)              |
