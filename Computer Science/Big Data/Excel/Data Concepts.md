Connects to: [[DAX]]
```toc
min_depth: 1
style: number
title: Table of Contents
```
# Granularity

```ad-summary 
title:Defintion 
Granularity is defined as the Size or level of detail of the entries in a table.

The more granular the more specific the entry, to reduce granularity we need to aggregate entries.
```

![[Pasted image 20230510133827.png]]

# Keys

```ad-summary 
title:Primary key 
Unique identifier for each row in a table so there are no duplicates. 

Usually primary keys are in the first column in Lookup tables. And are used on the one-side of a one-to-many relationship.
```

```ad-summary 
title:Foreign Key
Column that is allowed duplicates and is used on the many-side of a one-to-many relationship
```


# Tables

```ad-summary 
title:Fact Tables
Table that stores the data to be summarized. They store the "facts" the measurements that we want to summarize (amount of sales or how many units). And foreign keys that we will use in relationships later.
```

![[Pasted image 20230510135253.png]]

```ad-summary 
title:Dimension Tables
First column is a Primary Key (PK) used in relatinoship with a Fact Table. 

The reamining columns are attributes that we can use as:
* Criteria or filters for reports and dashboards
* Values to lookup
* Helper values (for calculations)
```

![[Pasted image 20230510135436.png]]

```ad-summary 
title:Date Table
Type of Dimension table required by MS Power Tools for DAX time intelligence Functions
```

![[Pasted image 20230510135550.png]]

# Data Models

The structure of a Data Model must come from the type of Measures & Reports that the Business Decision Maker requires. 

Data Models can be stored in Power Pivot & Power BI Desktop.

Data Models can contain: [[Data Concepts#Tables |Fact Tables]], [[Data Concepts#Tables |Dimension Tables]], Relationships, Helper Columns, DAX Calculated Columns, DAX Measures Hidden / Not Hidden Tables and columns.

## Requirements for a good Data Model

1. Contains necessary data for end solution
2. Easy for decision maker to use
3. Allows fast queries (change criteria and solution updates quickly)
4. Is easy to update when new data is available
5. Easy to update structurally, if needed

 