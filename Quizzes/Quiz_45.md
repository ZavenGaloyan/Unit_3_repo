# Quiz 45
## SQL
```.py
Select sum(amount) from transactions where transaction_type is "deposit" group by account_id;
Select sum(amount) from transactions where transaction_type is "withdraw" group by account_id;

Select * from customers where customer_id=12;
```
