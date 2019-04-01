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
There are times that instead of counting or summing you simply want to get the maximum or minimum value of a particular column. As an experienced spreadsheets user you are certainly familiar with the MAX and MIN functions.


---
## Max and Min in Spreadsheets

```yaml
type: "FullSlide"
key: "5d44df30b4"
hide_title: false
```

`@part1`
![Test](https://assets.datacamp.com/production/repositories/4833/datasets/8955749e97c652135520e0da942a046d96bc5e77/Screenshot%202019-03-31%2009.56.01.png)


`@script`
Max and Min in SQL are very similar. In this sample spreadsheet of our podcast table we are pulling both the max and min of the episodes and total time in minutes columns. We can do the same thing in SQL.


---
## Max in SQL	

```yaml
type: "FullSlide"
key: "e3999ef6b7"
```

`@part1`
podcasts table
![](https://assets.datacamp.com/production/repositories/4833/datasets/5f43b9a3c9d1fcbc591e475b172244c5b0d5a90b/Screenshot%202019-03-31%2010.08.57.png)

```
SELECT MAX(episodes)
FROM podcasts
```


`@script`
First lets like at Max. Here we the same dataset as in our spreadsheet but stored in a SQL table. We want to get highest number from the episodes column. Just as in our previous aggregation exercises, we write a SELECT FROM statement. In this example we leave out the GROUP BY statement because we are not including any additional columns.


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
SELECT MAX() 
FROM podcasts
```
&nbsp;

# Result 
![](https://assets.datacamp.com/production/repositories/4833/datasets/02726a8eae58b6cae2b32d71a5e65e613651159a/Screenshot%202019-03-30%2023.08.17.png)


`@part2`



`@script`



---
## Max in SQL - with Group By 

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
```


`@part2`
Result
![](https://assets.datacamp.com/production/repositories/4833/datasets/a9642317eab31cc76813ab44033a2034ace60a4a/Screenshot%202019-03-31%2010.38.56.png)


`@script`
Now lets say you want to get the max number of episodes by category. This is where the the power of SQL comes in compared to spreadsheets. You simply add the additional column you want into your query. You also need to add a group by statement 

You have already learned how to use group by in the previous lessons covering count and sum.


---
## Let's practice!

```yaml
type: "FinalSlide"
key: "1821a73e4e"
```

`@script`


