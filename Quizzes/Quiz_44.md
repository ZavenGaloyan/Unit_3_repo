 # Quiz 44
 ## SQL
 ```.py
SELECT count(*) from INHABITANT where gender="Male" and state="Friendly";

Select avg(gold) from INHABITANT GROUP BY villageid;

Select count(item) from ITEM where item like  "A%";

Select count(DISTINCT job) from INHABITANT;

SELECT personid from INHABITANT where job is "Herbalist";

SELECT  item from ITEM where owner=4 or owner=18;
 ```
