# SQL Final Project

In this project, we are analyzing a dataset for a government agency containing consumer complaints recieved by financial institutions in 2013-2015.

## Getting Started

In order to get started, I first loaded the dataset into SQL. I first started the mysql server then created and used a database entitled final_project. I then loaded the datatable into sql.


```

### Queries

In order to determine which companies had the most complaints filed against them, I wrote code to filter the 5 companies who had the most complaints.

```
mysql> select company, COUNT(company) AS MOST_FREQUENT
    -> from data where company !=""
    -> GROUP BY company
    -> ORDER BY COUNT(company) DESC
    -> LIMIT 5;
```

In order to determine whether particular areas compalined about certain things, I wrote code to determine the number of complaints per location. 

```
mysql> select state_name, COUNT(state_name) AS MOST_FREQUENT
    -> from data where state_name !=""
    -> GROUP BY state_name
    -> ORDER BY COUNT(state_name) DESC
    -> LIMIT 5;

```
And finally, in order to determine the speed at which different locations responded to complaints, I filtered the top 5 companies with the most "yes" answers for timely_response.

```
mysql> select company, COUNT(company) AS MOST_FREQUENT
    -> from data where timely_response= "Yes"
    -> GROUP BY COMPANY
    -> ORDER BY COUNT(company) DESC
    -> LIMIT 5;

```
## Conclusion
In conclusion, the compnay Experian had the most complaints filed against it, California had a large number of complaints, and Experian also had the most time effective response time for complaints.







