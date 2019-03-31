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
There are times that instead of counting or summing you simply want to get the maximum or minimum value of a particular column.


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
As an experienced spreadsheets user you are certainly familiar with the MAX and MIN functions. Max and Min work very similarly with some additional capabilities.


---
## Max in SQL	

```yaml
type: "FullSlide"
key: "e3999ef6b7"
```

`@part1`
![](https://assets.datacamp.com/production/repositories/4833/datasets/5f43b9a3c9d1fcbc591e475b172244c5b0d5a90b/Screenshot%202019-03-31%2010.08.57.png)


`@script`
Here we have the same list of podcasts from our excel sheet but stored in a SQL table. We want to get the max of the episodes column.


---
## Max in SQL

```yaml
type: "TwoRows"
key: "cadca73a6a"
```

`@part1`
Max in SQL 
```
SELECT MAX()
FROM podcasts
```


`@part2`
Result
![](https://assets.datacamp.com/production/repositories/4833/datasets/02726a8eae58b6cae2b32d71a5e65e613651159a/Screenshot%202019-03-30%2023.08.17.png)


`@script`



---
## Max in SQL - with names

```yaml
type: "TwoRows"
key: "d8082fbb09"
```

`@part1`
SQL
```
SELECT name, max(episodes)
FROM podcasts
```


`@part2`



`@script`



---
## Let's practice!

```yaml
type: "FinalSlide"
key: "1821a73e4e"
```

`@script`


