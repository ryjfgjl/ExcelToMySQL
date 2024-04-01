
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6t3n0o6au33c6t5cxsmq.png)

## What is it?
**ExcelToMySQL** is a productivity tool that can automatically import excel into mysql. ***Automation*** is its main feature, because it can automatically generate table information based on excel to establish contact with the database, and finally import the data into the database table. ***Batch*** is another feature of it, because it can be automated, so you can import thousands of tables at one time instead of importing them one by one. ***Scheduled*** import and export, real-time refresh, to achieve seamless connection between Excel data and database table data.

## Features
### Automatic
  The tool can automatically generate table names, column names, column types and lengths based on excel, and finally create tables and import data, or automatically match and append or update data based on the generated table information and database tables.
  
### Batch
  Usually you can only use other tools to manually import excel into the database one by one, but now, you can import thousands of tables at once.

### Simple
  Just provide the excel file location and target database connection information, and the tool will start working until all excel is imported.

### Fast
  It takes 3s to import all 10 excel sheets with 10,000 rows x 20 columns x 1MB each. 
  It only takes 3m24s to import a large excel with 1 million rows x 50 columns x 300MB.
  It only takes 5m35s to import a giant csv with 10 million rows x 30 columns x 4GB. 
  and importing a giant excel with 10 sheets totaling 10 million rows x 50 columns x 2GB only takes 31m25s 
  (normal notebook test)

### Smart
  Do you often encounter errors when importing manually? do not worry! Tools can easily avoid or automatically correct them.

### Timing
  You can use the built-in scheduled task function or combine it with other scheduled task programs to achieve scheduled import.

### Real-time
  Using scheduled tasks, when excel data is updated, it can be updated synchronously to the database in real-time.
  
### Security
  The software is green and requires no installation, and can work under any network conditions.


# Introduction and Download of ExcelToDatabase

[ExcelToDatabase - Automation tool for batch importing Excel files into database](https://github.com/ryjfgjl/ExcelToDatabase/blob/master/README.md)
