# Data-pipeline-in-Informatica-SCD-Type2

In Type 2 Slowly Changing Dimension, a new record is added to the table to represent the new 
information. Therefore, both the original and the new record will be present. The new record gets its 
own primary key.

In our example, recall we originally have the following table:
Customer Key Name State
1001 Christina Illinois

After Christina moved from Illinois to California, we add the new information as a new row into the 
table:

Customer Key Name State
1001 Christina Illinois
1005 Christina California

Advantages:
- This allows us to accurately keep all historical information.
Disadvantages:
- This will cause the size of the table to grow fast. In cases where the number of rows for the table is 
very high to start with, storage and performance can become a concern.
- This necessarily complicates the ETL process.
- 
Usage:
About 50% of the time.
When to use Type 2:
Type 2 slowly changing dimension should be used when it is necessary for the data warehouse to 
track historical changes
