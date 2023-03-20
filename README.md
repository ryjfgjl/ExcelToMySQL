# ExcelToMySQL: batch import excel files into mysql database automatically
<img width="733" alt="image" src="https://user-images.githubusercontent.com/39375647/222678425-2abecaab-b0fb-4a2c-9385-8f595c0f12b4.png">



## What is it?
**ExcelToMySQL** is an automatical tool which can batch import multiple excel files into (mysql database. *Automation* is its main feature  beacuse the tool can import data into database automatically and no need you to provide a setting. *Batch* is the another feature beacuse of automation, so you can import 10 or 10000 excels one time but not one by one.

## Features
### Automation
  Based on the excel, the tool can create table and import data into the database automatically, or just append/merge the data based on the automatical mapping between the excel and databases.
  
### Batch
  Usually you only can import excel one by one using the other tool. But now, you can import all excels you want one time.

### Easy
  You only need to provide the location of excels and the connect information of database, the tool can work until all the excels are imported

### Fast: 
  Only 10s to import 10 excels completely, containing 10000 rows x 10 columns each of them

### Intelligent: 
  When you manually import excel into database, whether if you feel sad when error occurs? DO NOT WORRY! The tool can deal with them!

### Advanced: 
  Rich options could be custom choose to make more fuction come true.

### Schedule: 
  You can make a schedule using it on windows/linux.
  
### Realtime
Sync data in excel into database in realtime.


## Where to get it

  The packaged executable program(ExcelToMySQL.exe on windows) is available, 
  
  you can download it from [sourceforge](https://sourceforge.net/projects/exceltomysqldb/).

<a href="https://sourceforge.net/projects/exceltomysqldb/files/latest/download"><img alt="Download ExcelToMySQL" src="https://a.fsdn.com/con/app/sf-download-button" width=276 height=48 srcset="https://a.fsdn.com/con/app/sf-download-button?button_size=2x 2x"></a>

## Menu

### Data Source
  * Files: choose Files as your data source, in this case, you can select one or more excel files to import
  * Directory: choose Directory as your data source, in this case, excels under the directory will be imported

## Excel：
  Choose files or directory as your data source

## MySQL Connection: 
  Input connection information of your target database

## Excel Options：
  #### Recursion of Directories
      Recursive directories to find all excel files
  #### Only Import Excel Last Modified
    Only Import Excel Last Modified since last imported.
  #### Encoding of CSV：
    Tools can auto-detect encoding of csv files(default), 
    and you can choose or input other value
  #### Field Name Row：
    The row number of field name in excel, default 1 if not populated
  #### First Data Row：
    The row number of data start in excel, default 2 if not populated
  #### Skip Footer Rows：
    The number of rows to skip on the foot of excel, default 0 if not populated
  #### Index or Name of Sheet to Import：
    assign the Sheet Index or Sheet Name to import
  #### Skip Sheet Which Name Start With：
    assign a character to skip sheet when sheet name start with it
  #### Trim Field Values：
    Remove spaces around the field value
  #### Replace Values to Null：
    values populated(comma separated) will be replaced to null

## Schedule Options：
  make a schedule, input a start time(default now if not populated) and a interval
  
## MySQL Options：
  #### Drop table if exists：
    drop table if exists
  #### Create table if not exists：
    create table if not exists
  #### Truncate Table Before
    Truncate Table Before Import
  #### Append All Data into One Table：
   import all data into the table populated
  #### Append Data into a same table in the case：
   import data to the table satify the case
  #### Increase column length when not enough
    Increase column length when it is not enough
  #### When excel has redundant column
    ignore redundant or add new
  #### When excel data duplicate with table
    ignore or update
  #### Add prefix for the created table names：
    The value populated will be added to table name before
  #### Add a key column which value is increament integerr：
    Add a key column which value is increament integer
  #### Save excel name to the column：
    Save excel name to the column
 

## How the tool works?
  Some logic is described below when the tool work
  ## How to define table name：
    If only one sheet in excel >> excel name
    If multipule sheets in excel >> excel name + '_' + sheet name
    Symbol like ',' will be replaced to '_'
    If table name is more than the limit of database >> cut off  
  ### How to define column name：
    Default is the first row, but if the first row is all blank, next row will be used
    Symbol like ',' will be replaced to '_'
    If column name is blank, 'unnamed' will be set as column name
    If column name is repeated, number like '0' will be added as its suffix
  ### How to define column type：
    Varchar(255) is default. If max length of column more than 255, text/clob will be set.
    
## How To Schedule
  The tool can directly run in command line without gui, so you can schedule it on the Windows or Linux. A configuration file(config.yaml) is needed to add.
    
    ExcelToMySQL.exe D:/config.yaml

# Getting Help
  * Email: ryjfgjl@qq.com
