# Data warehouse Modelling

- In DWM, the goal is to organize data in such a way that it can be easily retrieved, analysed and understood.
- Since warehouses are only for decision support, not for day-to-day transactions we use **multidimensional data models** to store the data.
- These models allow the analysts to look at data from different dimensions ie., date,time,location.

- The main concepts here are Data Cubes, Star Schema, Snowflake Schema, Fact Constellation Schema

## Data Cube

- A data cube allows data to be viewed in multiple dimesnions.
- It is defined by Dimensions and Facts.

### Dimensions

- Dimensions are the perspectives with respect to which an organisation wants to store or keep the data.
- For example a sales company may store data in terms of date, time, location etc.
- Each dimension has a table associated to it known as the **Dimension Table**, which further describes the dimension.
- For the dimension **time**, the dimension table may contain attributes like item_name, item_type etc.


### Facts

- A mutlidimensional data model is typically organized around a central theme, and that theme is represented by the fact table.
- For example for a sales datawarehouse, the facts include dollars_sold, units_sold.

----------------------------------------------------------------------------------------------------------------------------------------

## Star Schema

- The most common modelling paradigm is the star schema, in which the data is stored in:
  - A fact table that is present in the centre which does not contain redundant data.
  - A set of smaller dimension tables for each dimesnion.

### 📎Disadvantages:

1. Data redundancy
2. Limited flexibility
3. Wasted storage

----------------------------------------------------------------------------------------------------------------------------------------------

## Snowflake Schema

- The snowflake schema is a variant of star schema, where data of some dimensional tables is normalised and therefore splitting the data into additional tables.

### Advantages

- The main difference between snowflake and star schema is that some of the dimensional tables of snowflake schema are normalised to reduce redundancy.
- Tables are simple and saves storage space.

### Disadvantages

- More joins are needed to execute a query.


---------------------------------------------------------------------------------------------------------------------------------------------

## Fact Constellation Schema

- Sophisticated applications may require multiple fact tables to share dimension tables.
- This type of schema appears as a collection of stars or a galaxy.
- Hence this schema is called as **Galaxy schema** or **Fact constellation schema**.
- A fact constellation schema allows dimension tables to be shared amond fact tables.

