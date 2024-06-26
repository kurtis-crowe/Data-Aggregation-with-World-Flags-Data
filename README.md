# Data Aggregation and Grouping
## Using World Flags Data

Aggregating and transforming data is a critical aspect of data analysis. After data preparation, it's often necessary to compute group statistics or create pivot tables for reporting or visualization purposes. Pandas' `groupby` functionality provides a flexible way to perform these aggregations and summarize datasets.

For this module, we'll work with data containing details of various nations and their flags. Originally collected from the 'Collins Gen Guide to Flags' by Collins Publishers in 1986, it's important to note that this dataset is outdated, still including 'USSR' as a country.

### Dataset Overview

- There are 194 instances (rows) in total.
- The dataset comprises 30 attributes (columns).
- 10 attributes are numeric-valued, while the rest are Boolean or nominal-valued.
- There are no missing values.

**Attribute Information**

1. name: Name of the country concerned
2. landmass: 1=N.America, 2=S.America, 3=Europe, 4=Africa, 5=Asia, 6=Oceania
3. zone: Geographic quadrant based on Greenwich and the Equator (1=NE, 2=SE, 3=SW, 4=NW)
4. area: in thousands of square km
5. population: in round millions
6. language: 1=English, 2=Spanish, 3=French, 4=German, 5=Slavic, 6=Other Indo-European, 7=Chinese, 8=Arabic, 9=Japanese/Turkish/Finnish/Magyar, 10=Others
7. religion: 0=Catholic, 1=Other Christian, 2=Muslim, 3=Buddhist, 4=Hindu, 5=Ethnic, 6=Marxist, 7=Others
8. bars: Number of vertical bars in the flag
9. stripes: Number of horizontal stripes in the flag
10. colors: Number of different colors in the flag
11. red: 0 if red absent, 1 if red present in the flag
12. green: same for green
13. blue: same for blue
14. gold: same for gold (also yellow)
15. white: same for white
16. black: same for black
17. orange: same for orange (also brown)
18. mainhue: predominant colour in the flag (tie-breaks decided by taking the topmost hue, if that fails then the most central hue, and if that fails the leftmost hue)
19. circles: Number of circles in the flag
20. crosses: Number of (upright) crosses
21. saltires: Number of diagonal crosses
22. quarters: Number of quartered sections
23. sunstars: Number of sun or star symbols
24. crescent: 1 if a crescent moon symbol present, else 0
25. triangle: 1 if any triangles present, 0 otherwise
26. icon: 1 if an inanimate image present (e.g., a boat), otherwise 0
27. animate: 1 if an animate image (e.g., an eagle, a tree, a human hand) present, 0 otherwise
28. text: 1 if any letters or writing on the flag (e.g., a motto or slogan), 0 otherwise
29. topleft: color in the top-left corner (moving right to decide tie-breaks)
30. botright: color in the bottom-left corner (moving left to decide tie-breaks)
