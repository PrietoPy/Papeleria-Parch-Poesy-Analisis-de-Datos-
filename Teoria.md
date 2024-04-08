## Lets get some practice using *ORDER BY*

1. Write a query to return thr 10 earliest orders in the **orders**. include the *id*, *occurred_at*, and *total_amt_usd*

```sql
Select id, occurred_at, total_amt_usd 
    from public.orders
    order by occurred_at
    LIMIT 10
```

2. Write a query to return the lowest 20 orders in terms of smallest **total_amt_usd* include the *id*, *account_id*, and *total_amt_usd*

```sql
Select id, occurred_at, total_amt_usd 
    from public.orders
    order by total_amt_usd desc
    LIMIT 5
```

3. Write a query to return the lowest 20 *orders* in terms of smallest *total_amt_usd**. include the *id*, *account_id*, and *total_amt_usd*

```sql
Select id, occurred_at, total_amt_usd 
    from public.orders
    order by total_amt_usd
    LIMIT 20
```

## Order By part II

1. Write a query that displays the order ID, account ID, and total dollar amount for all the orders, sorted first by the account ID (in ascending order), and then by the total dollar amount (in descending order).

```sql
   Select id, account_id, total_amt_usd
       from orders
       order by account_id, total_amt_usd desc
```

2. Now write a query that again displays order ID, account ID, and total dollar amount for each order, but this time sorted first by total dollar amount (in descending order), and then by account ID (in ascending order).
   
   ```sql
   select id, account_id, total_amt_usd
       from orders
   order by total_amt_usd desc, account_id
   ```
   
   

3. Compare the results of these two queries above. How are the results different when you switch the column you sort on first?
   
   the hav completly diferent data

4. 
