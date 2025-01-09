# **Go Genesis**

**Go Genesis** is an open-source library designed to simplify the process of seeding your existing database. With this library, you can achieve the following:

- **Generate Go Models**: Automatically generate Go structs with the necessary struct tags.
- **Seed the Database**: Populate your database using code-generated data.



## **Advantages**

Using Go Genesis comes with several benefits:

1. **No Need for Existing Seed Files**  
   The library generates seed data dynamically at runtime.

2. **Automatic Priority Calculation**  
   The library calculates the priority order of tables for insertion, handling foreign key constraints seamlessly.



## **Problem Statement**

Seeding a database in a development environment is often a challenging task. Manually inserting rows becomes tedious, especially when dealing with complex foreign key constraints.



## **Solution Strategy**

Go Genesis addresses this issue by automating the procedural aspects of database seeding. The solution involves the following steps:

1. **Generate Go Models**  
   Create Go structs directly from your database schema, complete with required struct tags.

2. **Calculate Table Priority**  
   Automatically determine the priority order of tables to ensure that foreign key constraints are respected during data insertion.

3. **Configuration via JSON**  
   A JSON configuration file is used to customize the behavior of the tool. This file includes:
   - The number of rows to be generated for each table.
   - The struct tags required in the generated models.
   - The file path where the generated models will be stored.

4. **Runtime Seed Data Generation**  
   - Read the column types of the database schema.
   - Construct and insert the seed data dynamically, without relying on pre-existing seed files.



By following these steps, **Go Genesis** automates the tedious task of database seeding, making the development process more efficient and error-free.
