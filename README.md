# Stat-Xplore API Query with Python

## Output

This Python script will successfully iterate through .json files stored in a file directory and query them using the Stat-Xplore API. It appends the return of each query and adds a new column labelling the file name of the query at the time to produce a resulting table that contains all values for all json files loaded and context around the origins of each value. 

This is useful given Stat-Xplore will likely return a 'Request Entity Too Large' issue if the custom table generated is too large. Batching the upload by region, for instance, proves a successful work-around.

This script can be executed within PowerBI.

## Requirements

- **The same data shape is queried for each json file.** *This is only intended to work with the same query adjusted for the similar type of row-level granularity. Making any adjustments will almost certainly result in an error message but is currently untested.*
- **The query files are saved as .json files**

  ## Creating Custom Table Queries in Stat-Xplore

Please use the below support documentation, as supplied and maintained by Stat-Xplore, for information on how to create custom tables. 

https://stat-xplore.dwp.gov.uk/webapi/online-help/Create-a-Custom-Group.html

It is important to download the query as a .json file.

## Known Improvements

- **Error Handling.**
- **File Management.** Processed files should be moved/deleted so as to reduce the likelihood json queries with different sizes are not appended to one another. 



