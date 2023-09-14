Data set from- https://www.kaggle.com/datasets/beekiran/sales-data-analysis

Questions
1) What was the best month for sales?
How much was earned that month?
```sql
SELECT sum(sales),month FROM sales_data GROUP BY month ORDER BY month DESC
```
Answer- 12

2)  What city sold the most product? 
```sql
SELECT city, sum(sales) from sales_data group by city order by sum(sales) DESC
```
Answer- SanFrancisco 

3) What time should we display advertisemens to maximize the likelihood of customer’s buying product? 
``` sql 
select sum (sales), hour from sales_data group by hour order by sum (sales) DESC 
```

Answer- My recommendation will be 19 or 7pm 

4) What product sold the most? 

``` sql
select count(product), product from sales_data group by product order by count(product) DESC 
```

Answer- USB-C Charging Cable
