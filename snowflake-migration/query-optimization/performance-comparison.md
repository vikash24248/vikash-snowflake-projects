## Before vs After Optimization

### Query:
Fetching monthly sales data across 4 regions with joins on 3 fact tables.

| Metric         | Before Optimization | After Optimization |
|----------------|---------------------|--------------------|
| Execution Time | 32 seconds          | 4.8 seconds        |
| Scan Volume    | 1.8 GB              | 300 MB             |
| Query Cost     | High                | Low                |

### Changes Applied:
- Rewrote `JOIN` logic with CTEs
- Replaced `SELECT *` with specific columns
- Used clustering on large fact table
