```ad-summary 
title:Defintion 
Data warehouse is an information system that contains historical and commutative data from single or multiple sources. It simplifies reporting and analysis process of the organization
```

# Characteristics

A data warehouse has the following characteristics
* Subject-Oriented
* Integrated
* Time-variant
* Non-volatile

## Subject-Oriented

```ad-summary 
title:Defintion 
A data warehouse is subject oriented as it offers information regarding a theme instead of a compoanies' ongoing operations. These subjects can be sales, marketing, distributions, etc...
```

A data warehouse never focuses on the ongoing operations. Instead, it puts emphasis on modeling and 
analysis of data for **decision making**. It also provides a simple and concise view around the specific subject by excluding data which not helpful to support the decision process

## Integrated

```ad-summary 
title:Defintion 
A data warehouse is developed by integrating data from varied sources like a mainframe, relational dtabases, flat files, etc... Moreover, it must keep consistent naming conventions, format, format and coding.
```

This integration helps in effective analysis of data. Consistency in naming conventions, attribute measures, encoding structure, etc... have to be ensured. 

![[Pasted image 20230420200557.png]]

## Time-Variant

The time horizon for data warehouse is quite extensive compared with operational systems. The data collected in a data warehouse is recognized with a particular period and offers information from the historical point of view. It contains an element of time, explicitly or implicitly.

One such place where Datawarehouse data display time varaince is in the structure of the record key. Every primary key contained with the DW should have either implicitly or explicitly an element of time. Like the day, week, month, etc. 

Another aspect of time variance is that once data is inserted in the warehouse, it can't be updated or changed.

## Non-volatile

```ad-summary 
title:Defintion 
DW are also non-volatiel, meaning that the previous data is not erased when new data enters in.


Data is read-only and periodically refreshed. This also helps to analyze historical data and understand what & when happened. It does not require transaction process, recovery, and concurrency control mechanisms
```

Activities like delete, update, and insert which are performed in an operational application environment are omitted in DW environment. Only two types of data operations are performed in DW: 

1. Data Loading
2. Data Access

# Differences between operational application and DW

| **Operational Application**                                                                                                    | **Data Warehouse**                                                        |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------- |
| Complex program must be coded to make sure that data upgrade processes maintain high integrity of the final product            | This kind of issues does not happen because data update is not performed. |
| Data is placed in a normalized form to ensure minimal redundancy                                                               | Data is not store in normalized form                                      |
| Techonology needed to support issues of transactions, data recovery, rollback, and resolution as its deadlock is quite complex | It offers relative simplicity in technology                               |


![[Pasted image 20230420201706.png]]