---
title: Insert title here
key: cff168ddadbf61da35eed7de862fec5f

---
## Getting the MAX (or MIN)

```yaml
type: "TitleSlide"
key: "d12a2e9d31"
```

`@lower_third`

name: Robert Ward
title: Data Scientist at Applied Information Sciences (AIS)


`@script`
There are times that instead of counting or summing you simply want to get the maximum or minimum value of a particular column from your dataset. As an experienced spreadsheet user you are most likely familiar with the MAX and MIN functions.


---
## Max and Min in Spreadsheets

```yaml
type: "FullSlide"
key: "5d44df30b4"
hide_title: false
```

`@part1`
![Test](https://assets.datacamp.com/production/repositories/4833/datasets/8955749e97c652135520e0da942a046d96bc5e77/Screenshot%202019-03-31%2009.56.01.png){{1}}


`@script`
Max and Min in SQL are very similar. In this spreadsheet containing our podcast table we are pulling both the max and min of the episodes and total time in minutes columns. We can do the same thing in SQL.


---
## Max in SQL

```yaml
type: "FullSlide"
key: "e3999ef6b7"
```

`@part1`
podcasts database table
![](https://assets.datacamp.com/production/repositories/4833/datasets/5f43b9a3c9d1fcbc591e475b172244c5b0d5a90b/Screenshot%202019-03-31%2010.08.57.png){{1}}

```
SELECT MAX(episodes)
FROM podcasts
```{{2}}


`@script`
Lets look at at Max for our first example. Here we have the same dataset as in our spreadsheet but stored in a SQL table. We want to find the highest number from the episodes column. Just as in our previous aggregation exercises, we write a SELECT statement followed by the function - SELECT Max(episodes) FROM podcasts. In this example we leave out the GROUP BY statement because we are did not add any additional columns.


---
## Max in SQL - one result

```yaml
type: "TwoRows"
key: "0e7b892510"
disable_transition: false
code_zoom: 100
```

`@part1`
```
SELECT MAX(episodes)
FROM podcasts
```
&nbsp;

# Result 
![](https://assets.datacamp.com/production/repositories/4833/datasets/02726a8eae58b6cae2b32d71a5e65e613651159a/Screenshot%202019-03-30%2023.08.17.png)


`@part2`



`@script`
Here you can see that the result of our query was just one number - the max number of episodes. Nice as that is, that may not be all the information we are after. We have no idea which podcast has the max number of episodes. If we want that, we need to add in the name column.


---
## MAX - with additional column(s)

```yaml
type: "FullSlide"
key: "32f5630f1c"
```

`@part1`
```
SELECT name, max(episodes)
FROM podcasts
```{{1}}
&nbsp;

![](https://assets.datacamp.com/production/repositories/4833/datasets/4ee42879d2003e5114f27acb7a413dd1d8fb45f8/Screenshot%202019-03-31%2022.37.37.png){{2}}


`@script`
Here we add an additional column - the name - and the resulting output is much more informative. The result is the same but also gives us the name of the podcast that has the most episodes.


---
## Get the Max by category?

```yaml
type: "FullSlide"
key: "0e735a1086"
```

`@part1`
podcasts table {{1}}

![](https://assets.datacamp.com/production/repositories/4833/datasets/5f43b9a3c9d1fcbc591e475b172244c5b0d5a90b/Screenshot%202019-03-31%2010.08.57.png){{2}}


`@script`
You may have noticed in our podcasts table that there was a category column. What if we wanted to get the max number of episodes by category?


---
## Max with Group By

```yaml
type: "TwoRows"
key: "d8082fbb09"
```

`@part1`
SQL 
```
SELECT category,  max(episodes)
FROM podcasts
GROUP BY category
```{{1}}


`@part2`
Result 
![](https://assets.datacamp.com/production/repositories/4833/datasets/a9642317eab31cc76813ab44033a2034ace60a4a/Screenshot%202019-03-31%2010.38.56.png){{2}}


`@script`
Once again we use the GROUP BY statement. So far GROUP BY has not been required when using MAX, but now that we are introducing additional columns it is.

Once again however this result by itself is not very useful.


---
## Max and Group By - Continued

```yaml
type: "TwoRows"
key: "32920ea9c7"
```

`@part1`
SQL 
```
SELECT name, category, max(episodes)
FROM podcasts
GROUP BY category
```{{1}}


`@part2`
Result 
![](https://assets.datacamp.com/production/repositories/4833/datasets/4f6f736113d5cbcbba04c8bf132f1f10603495dd/Screenshot%202019-03-31%2023.13.37.png){{2}}


`@script`
Now that we add the name column, querying for the max episodes by category is a lot more useful. Note that we only needed to GROUP BY category. This is a little different than grouping by with SUM as the database is not doing any adding. It is simply taking the max of each category. If we gave the group by statement both name and category, it would return the entire table! This is because each name is unique and by default the episode count is the max of each of those names.


---
## SQL MIN - the same but opposite

```yaml
type: "FullSlide"
key: "d9c4372b66"
```

`@part1`



`@script`
You will practice with Min in the exercises but I will quickly touch on it here. Min works exactly the same as Max does in all of these examples with the exception that it returns the smallest number instead of the largest. That is the only difference.


---
## Let's practice!

```yaml
type: "FinalSlide"
key: "1821a73e4e"
```

`@script`


