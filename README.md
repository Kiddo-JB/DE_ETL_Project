# DE_ETL_Project
This project demonstrates a simple Extract, Transform, Load (ETL) process using Python. The goal is to extract data from multiple file formats (CSV, JSON, and XML), transform it (e.g., perform unit conversions), and load the transformed data into a structured format (CSV).

Features

**Extract:** Supports extracting data from CSV, JSON (in NDJSON format), and XML files.

Transform: Performs unit conversions for height (inches to meters) and weight (pounds to kilograms), rounding the results to two decimal places.

**Load:** Saves the transformed data into a new CSV file.

Logging: Tracks the progress of each ETL step, saving log messages to a text file for traceability.

**Prerequisites**

**Libraries**

Ensure you have the following Python libraries installed:

1.pandas

2.json

3.xml.etree.ElementTree (built-in)

4.datetime (built-in)

Install pandas using pip if not already installed:

**Usage**

**Step 1:** Upload Source Files

Upload your source files (CSV, JSON, XML) to the working directory.

**Step 2:** Update File Paths

Update the paths for your source files in the file_paths list.

**Step 3**: Run the Script

Run the script using the following example:

    file_paths = ['./source1.csv', './source1.json', './source1.xml','./source2.csv', './source2.json', './source2.xml','./source3.csv', './source3.json', './source3.xml']
    etl_process(file_paths, TRANSFORMED_DATA)

**Output**
  Transformed data is saved to the specified CSV file (/content/transformed_data.csv).

  Logs of the ETL process are saved in a text file (/content/log_file.txt).

**Code Overview
  Key Functions**
  
   **1.Extract Functions:**
    
        extract_csv: Reads data from a CSV file.
    
        extract_json: Reads data from a JSON file (in NDJSON format).
    
        extract_xml: Parses data from an XML file.
    
        extract_data: Combines data from multiple source files into a single DataFrame, removing duplicates.
    
    **2.Transform Function:**
    
        transform_data: Converts height from inches to meters and weight from pounds to kilograms, rounding to 2 decimal places.
    
    **3.Load Function:**
    
        load_data: Writes the transformed data to a CSV file.
    
    **4.ETL Process:**
    
        etl_process: Orchestrates the entire Extract, Transform, and Load workflow.

