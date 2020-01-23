## Day 4 - Data management with SQL

The SQL database was created by clicking the option 'New Database' in the top left corner 
of the DB Browser for SQLite and subsequently choosing the four text files to add to the 
database.

### Question 1: 
How many species of the _Charadriiformes_ order have an omnivore diet?

-	Diet-5Cat was renamed to DietCat because SQLite did not understand ‘5Cat’.

    Code used in SQLite:

```sql
SELECT IOCOrder , DietCat, COUNT(*) AS answer
FROM BirdFuncDat
WHERE DietCat IS 'Omnivore'
GROUP BY DietCat, IOCOrder;
``` 

- Answer: **39** bird species. </br></br>

### Question 2:
What is the average body mass value of the _Tyrannidae_ family, rounded up?

-	BodyMass-Value was renamed to BodyMassValue because SQLite did not understand ‘-Value’.

    Code used in SQLite:

```sql
SELECT BLFamilyLatin, ROUND(AVG(BodyMassValue))
FROM BirdFuncDat
WHERE BLFamilyLatin = 'Tyrannidae';
``` 

- Answer: **18.0**

