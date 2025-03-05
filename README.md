# bank-data-sql-analysis
Project to analyse UCI bank marketing dataset by using SQL queries and SQlite.

# Data

1. Download dataset : https://archive.ics.uci.edu/dataset/222/bank+marketing

2. Replace from .csv file the characters
; -> , and " -> '
This is done to ensure 

# Setup (for Windows OS)
1. If you haven’t installed yet, get the SQLite and SQLite Studio.

2. Prepare the Dataset
   
Place the dataset it in data/bank_cleaned.csv.
Navigate to your project folder where your SQLite database will be stored

4. Create the Database
   
Run the following commands in Command Prompt (cmd.exe):

sqlite3 bank.db
.mode csv

4. Create the Table Structure

CREATE TABLE bank (
  age INTEGER,
  job TEXT,
  marital TEXT,
  education TEXT,
  default TEXT,
  balance INTEGER,
  housing TEXT,
  loan TEXT,
  contact TEXT,
  day INTEGER,
  month TEXT,
  duration INTEGER,
  campaign INTEGER,
  pdays INTEGER,
  previous INTEGER,
  poutcome TEXT,
  y TEXT
);

Make sure the table schema matches the CSV data.

4. Import data

Connect to the database with SQLite. Go to Tools -> Import
Data Source Type -> CSV 
Column separator -> Comma

Modify the above if necessary.

5. Verify data import

In project folder run:

sqlite3 bank.db ".tables"
sqlite3 bank.db "SELECT * FROM bank LIMIT 5;"

