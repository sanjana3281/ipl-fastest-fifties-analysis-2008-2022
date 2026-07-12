# ipl-fastest-fifties-analysis-2008-2022

## Dataset
IPL Complete Dataset 2008-2022 from Kaggle — 1484 records of fastest fifties scored across all IPL seasons.

## Questions & Findings

### 1. Who scored the most fastest fifties?
SELECT 
       against,
       count(*) as num
    FROM fastest_fifties_all
    GROUP BY against 
    order by num desc
    limit 1
Finding: David Warner

### 2. Which ground hosted the most fastest fifties?
SELECT 
     against,
     count(*) as num
  FROM fastest_fifties_all
  GROUP BY against 
  order by num desc
  limit 1
Finding:Wankhede Stadium

### 3. Who hit the fastest fifty ever?
SELECT player, bf
  FROM fastest_fifties_all
  ORDER BY bf ASC
  LIMIT 1
Finding: Pat Cummins

 ###4. Which year had the most fastest fifties?
 SELECT 
        SUBSTR(match_date, -4) as year,
        COUNT(*) as total
    FROM fastest_fifties_all
    GROUP BY SUBSTR(match_date, -4)
    ORDER BY total DESC
    LIMIT 1
Finding:2022

### 5. Which team conceded the most fastest fifties?
SELECT 
     against,
     count(*) as num
  FROM fastest_fifties_all
  GROUP BY against 
  order by num desc
  limit 1
Finding: PBKS
