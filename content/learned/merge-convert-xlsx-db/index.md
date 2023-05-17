---
title: Convert and merge xlsx files into a db
summary: a BASH script to create a db from separate xlsx files
date: 2023-05-10
lastmod: 2023-05-10
tags: [ Linux, BASH, SQL ]
---

```bash
 #!/bin/bash

# Loop through all xlsx files in the current directory
for file in *.xlsx
do
    # Convert xlsx file to csv format using xlsx2csv
    xlsx2csv "$file" "${file%.xlsx}.csv"
done

# Combine all csv files into a single file
cat *.csv > combined.csv

#create database
sqlite3 combined.db <<EOF
CREATE TABLE combined (
    Entry VARCHAR, 
    Ref FLOAT, 
    ...
);
EOF

# Import the content from the combined.csv file
sqlite3 combined.db <<EOF
.mode csv
.import combined.csv combined
EOF
```

