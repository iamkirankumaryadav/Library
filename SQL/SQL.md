# SQL    (DB : Data Base)
Structured Query Language
Core of Relational DB used to Access and Manage DB

Data Mart > Data Warehouse > Data Base > Table

Row | Record

Column | Field | Key

Page : Basic Unit of Database File (I/O)

NULL : Unavailable | Unknown | Unassigned | NA

Zero | 0 : Number

blank space (' ' | " ") : Character 

Metadata : Data | Attributes about Data | Data that Describes Information about other Data.

Current Date : GetDate() Date + Timestamp

# Query Optimization
- Determine the most Efficient way to Execute a given Query by considering every Query Plan
  Large number of Queries can be Executed in Less Time 
  Reduce Time and Space Complexity.

# Subsets of SQL
DDL (Definition) : Define Data Structure | CREATE | ALTER | DROP | RENAME | TRUNCATE | COMMENT
DQL (Query) : Retrieve Data from DB SELECT  
DML (Manipulation) : Manupulate Data in DB - INSERT | UPDATE | DELETE | MERGE
DCL (Control) : Control Access to Data store in DB - GRANT | REVOKE

# DBMS
S/W Application
Allow user to Interact with Database

# Types of Database
- Relational : Structured Database | Data is stored in Relations (Tables)
  Non Relational : NoSQL | Data in the form of Dictionary (Key Value Pairs) | MongoDB

# Database Engine
  (Oracle, SQL Server, DB2, MySQL, PostgreSQL)
- Data Repository (Tables | Procedures | Functions | Views) related to Organization and Business or Personal Database.
- PostgreSQL is Free Open Source | Developed by Community of Developers

# ACID Properties
- A : Atomicity | All or Nothing
  C : Consistency | Gurantees Committed Transaction State | Data Meet All Validation Rules
  I : Isolation | Transparent and Independent | Concurrency
  D : Durability | Commited Data is Never Lost

# Data Integrity
- Accuracy as well as the Consistency of Data stored in DB

# Concurrency
- Two or more Computing Process Executing at the Same Time.

# Connection 
- The Means of Communication between a Client and a Server.

# Deadlock 
- A State in which Resource is Occupied by Two or More Process
  Process is Requesting for Resource which is already occupied by some other Process.

# View 
- Logical Representation of One or More Tables.

# Geospatial Data Type
- Data Types which are Specificially Optimized for Storage of Geographic Coordinate based Data.

# Hash
- An Indexing Method provided for Fast Retrieval.

# Inner Join
- Join between Two Tables where only the Rows with Matching Foreign and Primary Key Values are returned.

# Join
- An Operation in which Rows of 1 Table are related to Rows of another through Common Column Value.

INNER : Return only Common | Matching Rows 

LEFT : Return All Rows from Left Table and Matching from Right Table

RIGHT : Return All Rows from Right Table and Matching from Left Table

FULL : Returns all the Records from Left and Right

# Modification Stored Procedure 
- An SQL Stored Procedure that contains 1 or more INSERT | UPDATE and DELETE Statements.

# Natural Join
- Join formed between two Tables with Same Column Name and Same Data Type.

# Cross Join
- Cross Product | Cartesian Product of Two Tables

# OOP 
- Programming Paradigm that relies on Concept of Class and Objects
  Stucture a S/W Program into Simple Reusable Blueprints used to Create Individual Instance of Class.

# Stored Procedure 
- Set of SQL Statements with an Assigned Name, stored in RDBMS as a Group, that can be Reused by Multiple Programs.

# CHAR vs VARCHAR
Both are Character Data Type
Char : Fixed Length
Varchar : Variable Length

# Primary Key 
- A Column (Collection) that Uniquely Identifies Each Row in Table.
- Uniquely Identifies a Single Row in the Table
- Null Values are not Allowed

# Constraints
- Specify Limitation on Data Types of the Table
1.NOT NULL : Column should not Accept Null Value
2.CHECK    : Integrity (Limit the Value Range that can be Placed in Column) e.g. Salary should be between 2L to 4L
3.DEFAULT  : Default Value for a Column 
4.UNIQUE   : Each and Every Value in the Column is Unique.
5.PRIMARY KEY : Uniquely Identify Each Row | No NULL Allowed
6.FOREIGN KEY : Link Two Tables Together | Identify Relationship between Tables by Referencing Columns.

# Delete vs Truncate
Delete : Delete a Row in a Table
         Rollback Data
         DML Command
         Slower

Truncate : Delete ALl the Rows from a Table
           Cannot Rollback Data
           DDL Command
           Faster
	
# Normalization 
- Way of Organizing Data in the Database.
  Divide Large Tables into Small Tables and Link them using Relationships
  Avoid Duplication and Redundancy

More Table with Less Rows 
Efficient Data Access	
Quick Search | Easy Modification
Compact Database

# Denormalization
- Add Redundant Data to one or more Tables.

# Entity
- A Person, Place or thing in the Real World about which Data is Stored in Database.

# Relationship
- Relation or Links between Entities that have something to do with each other.

# Index 
- Index Refers to a Record or Row for Retrieval of Data

Unique Index : Each and Every Index Value is Unique (AUTONUM)

Clustered Index : Group of Index (Age between 5 to 18) | (States)

Non Clustered : Maintain Logical Order | Alphabetical (A to Z) or Ascending | Descending

# Trigger 
- Special Type of Stored Procedure 
  Defined to Execute Automatically after Data Modification
  Allows to Execute Batch of Process (Insert | Update | Delete Queries)

# Sub Query 
- A Query inside another Query defined to Retrieve Data 
  Outer Query is the Main Query and Inner Query is Sub Query
  Sub Query is Executed before Main Query
  Can be Nested inside a SELECT | UPDATE or any other Query
  Can also use any Comparison Operators.

# Correlated Sub Query
- Select the Data from a Table Referenced in the outer Query | Dependent on Column of Other Tabl

# Non Correlated Sub Query
- Independent Query | Output of Sub Query is Substituted in the Main Query.

# Group Function | Aggregate 
- Evaluate Mathematical Calculation and Return Single Value.
- Work on the Set of Rows and Result one Result Per Group. (AVG | COUNT | MAX | MIN | SUM | VARIANCE)

# Scalar Function
- Single Value based on Input e.g. NOW()

# BETWEEN vs IN

Between : Range                           e.g BETWEEN 5 AND 10
In : Check for Specific Values Provided   e.g. Value IN (5,6,7,8,9,10)

# Use of SQL Functions
1.Perform Some Calculations on the Data
2.Modify Individual Data Items
3.Manipulate Output
4.Format Dates and Numbers
5.Convert Data Types

# MERGE Statement

Allows Conditional Update or Insertion of Data into a Table

Performs Update : If Rows Exists.
Performs Insert : If the Row does not Exist.

# CLAUSE (WHERE | HAVING)
- Limit the Result
  Provide Condition to Query
  Filter the Rows 

Column Level Constraints :Limitations applied on Column
Table Level Constraints : Limitations applied on Entire Table

# Pattern Matching

Like (%) : Match Zero or More Character

Underscore (_) : Match Exactly One Character

Unique : DISTINCT

# View 

- Virtual Table | Subset of Data | Data of One or More Table combined on Relationship
  Restrict Access to Orignal Data Table
  Make Simple Query | Focus on Required Data
  Ensure Data Independence

# Collation
- Set of Rules that Determines How to Store and Compare Data.

# Local : Variable can be Accessed | Used | Exist only inside particular Function.
# Global : Variable can be Accessed throughout the Program

# Stuff vs Replace
  Stuff : Overwrite Existing Character | Part of Character | Add or Insert String into Existing String

  Replace : Replace the Existing Character and all its Occurence
