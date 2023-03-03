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

#### MySQL Connection: 
  Input connection information of your target database

### Excel Options：
  #### Recursion of Directories
      Recursive directories to find all excel files
  #### Only Import Excel Last Modified
    Only Import Excel Last Modified since last imported.
  #### Encoding of CSV：
    Tools can auto-detect encoding of csv files(default), 
    and you can choose or input other value
  #### Replace Values to Null：
    values populated(comma separated) will be replaced to null
  #### The Header on Row：
    Set which row as Column name
  #### The Data Start From Row：
    The data start from the row
  #### Trim Spaces：
    Trim spaces around the data


  #### Append All Data to One Exists Table：
    Under Append mode, import all data to the table populated
  #### Truncate Target Table Before Append
    Truncate Target Table Before Append
  #### Transform Chinese in Table/Column Name to The First Letter
    Transform chinese in table name and column name to the first letter of its pinyin
  #### Add Table Prefix：
    The value populated will be added to table name before
  #### Add a Key Column, Value is The Row Number：
    Add a Key Column, Value is The Row Number
  #### Add a Column, Values is The Excel Name：
    For imported table, add a column which value is its excel name
  
  #### Run Sql Before Starting
    When starting import, run sql in the sql file choosed before
  #### Run Sql After Comleting
    When complete import, run sql in the sql file choosed after
  #### Save Current Configuration
    Save Current Configuration
  #### Load Saved Configuration
    Load Saved Configuration

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
