# Aggregations

[1. Aggregate Functions](#1-aggregate-functions)

---

### 1. Aggregate Functions

| Function              | Returns                                  | NULL Behavior                            |
| --------------------- | ---------------------------------------- | ---------------------------------------- |
| `MIN(col)`            | Minimum value                            | Ignores NULLs                            |
| `MAX(col)`            | Maximum value                            | Ignores NULLs                            |
| `COUNT(*)`            | Count of all rows (including duplicates) | Counts rows with NULLs                   |
| `COUNT(col)`          | Count of non-NULL values in column       | Ignores NULLs                            |
| `COUNT(DISTINCT col)` | Count of unique non-NULL values          | Ignores NULLs                            |
| `SUM(col)`            | Sum of all values                        | Ignores NULLs; returns NULL if all NULLs |
| `AVG(col)`            | Average (mean) of values                 | Ignores NULLs; returns NULL if all NULLs |
| `STDDEV(col)`         | Standard deviation                       | Ignores NULLs                            |
| `VARIANCE(col)`       | Variance                                 | Ignores NULLs                            |

