# PRICE-RISK-MANAGEMENT-AND-PRICE-FORECASTING
This is end to end microsoft fabric project that analyze and predict price  



https://github.com/user-attachments/assets/ea9ffae9-a853-4c30-bbba-f026bd87f2c2


first ingest data into lakehouse ...through upload method...in warehouse schema we can get data fthrough  datflow or pipeline in warehouse then add shortcut to load that data data into lakehouse ...ingest data through into various types through database..pipeline ..shortcut..dataflow...and Turn CSV files to tables using the “Load to Tables” and now lakehouse shifted to sql analytics endpoint mode...Create relationships between the tables ... Create measures of various aggregate functions..built power bi report on basis of total order presented according to month country

# Getting Data Into Lakehouse
<img width="1486" height="603" alt="image" src="https://github.com/user-attachments/assets/4aaeef47-76ed-4b49-ad06-87d23920fc1e" />

# 1.Upload(direct upload table from csv)
we can upload files from local machine directly 
there are three types of files :structured ,semi-structured,unstructured
Structured files are organized in a table-like schema, while unstructured files lack any such organization, and semi-structured files fall in between.
Based on the provided descriptions, files can be derived as structured or unstructured based on whether they have a predefined, fixed format. Structured files are organized in a table-like schema, while unstructured files lack any such organization, and semi-structured files fall in between.

**Structured Files**
This fixed schema makes the data easy to query and analyze directly.
CSV (.csv):  Each line in the file represents a row, and commas separate the values into distinct columns. Its simple, tabular nature allows it to be easily parsed and loaded into databases or spreadsheets.
Excel (.xlsx, .xls):  The data is organized into cells, rows, and columns, with the added capability of containing multiple sheets and advanced formatting, which maintains its structured nature.
Parquet (.parquet): This is a highly optimized structured file format. It stores data in a columnar fashion, meaning all values from a single column are stored together. 

**Unstructured Files**
Unstructured files do not follow any predefined schema or format. 
Text (.txt):  A basic text file is simply a stream of characters without any inherent tags, separators, or organization.

**Semi-structured Files**
Semi-structured files are a hybrid that contain some organizational properties but do not fit into a rigid, tabular model. They use tags or key-value pairs to organize data, but the fields may be nested, optional, or have a variable number of attributes.
JSON (.json): It uses nested key-value pairs to represent data. While it has a defined hierarchy, not every record has to contain the same fields, and the structure can be more complex than a simple table. 

# 2.Start with sample data
we can upload sample data through sample datasets.
<img width="1218" height="341" alt="image" src="https://github.com/user-attachments/assets/24f6962e-da9e-48dc-a070-db11949c6853" />

# 3.Shortcut to Warehouse(a fact table)
<img width="1532" height="814" alt="image" src="https://github.com/user-attachments/assets/7ee10022-4ac6-4570-849f-3b0ac6fc2535" />

# 4.DataFlow
# 5.Data Factory pipeline

