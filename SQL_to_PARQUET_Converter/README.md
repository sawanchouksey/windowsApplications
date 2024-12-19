# SQL to Parquet Converter

The **SQL to Parquet Converter** is a Python-based application designed to convert tables from a SQL Server database into Parquet files. This tool is especially useful for users who want to export large datasets to the efficient Parquet format, a columnar storage file format known for its performance and compression benefits. The converter works by connecting to a SQL Server database, extracting all tables, and saving each one as a Parquet file, with optional compression.

## Key Features:
- **SQL Server to Parquet Conversion:** Extract tables from a SQL Server database and save them as Parquet files.
- **Customizable Output:** Choose the output directory and compression method (e.g., Snappy).
- **Logging:** Detailed logging to both file and console for transparency and error handling.
- **Progress Tracking:** Real-time progress bar with **TQDM** for tracking the status of the table conversions.
- **Automatic Configuration:** Default configuration is created if none exists, allowing easy setup.
- **Error Handling:** Detailed error messages and logging for each table conversion attempt.

## Technology Stack

This application is built using the following technologies:

1. **Python** – The primary programming language used for developing the application.
2. **pyodbc** – A Python library for connecting to SQL Server databases, used to fetch data from SQL Server tables.
3. **Pandas** – Utilized for reading SQL queries into DataFrames and exporting them as Parquet files.
4. **Parquet** – The Parquet file format is used for efficient columnar storage and compression.
5. **ConfigParser** – Used for reading and writing configuration files (e.g., database credentials and output settings).
6. **TQDM** – A Python library for displaying a progress bar, used to track the conversion progress for tables.
7. **Logging** – Provides a logging mechanism that records events and errors during execution.
8. **Datetime** – For timestamping log filenames and managing logs.

## How to Use

1. **Initial Setup:**
   - The first time you run the application, it will create a `config.ini` file if one does not already exist. The default configuration needs to be updated with your database credentials (server, username, password, etc.).

2. **Configure Database:**
   - Open the `config.ini` file and enter your database connection details:
     - **server**: The SQL Server address.
     - **database**: The name of the database.
     - **username** and **password** (optional) if not using a trusted connection.
     - **trusted_connection**: Set to 'yes' for Windows Authentication, or 'no' if using SQL Server Authentication.
  
3. **Run the Converter:**
   - Execute the application by running `SQLToParquet.exe` from the command line.
   - The program will connect to the database, retrieve a list of tables, and begin converting them to Parquet format.

4. **View Logs:**
   - A log file will be generated in the same directory as the application. The log file will contain detailed information about the conversion process, including any errors encountered during the process.

5. **Output Files:**
   - The Parquet files will be saved to the directory specified in the `config.ini` under the `OUTPUT` section (`parquet_files` by default).
   - The tables are saved in folders named after their schema.

## Configuration

The `config.ini` file contains the following sections and settings:

### DATABASE Section
- **server**: The server hosting the SQL Server instance.
- **database**: The name of the database you want to export.
- **trusted_connection**: If 'yes', the Windows authentication method will be used. If 'no', provide the `username` and `password`.
- **username**: Your SQL Server username (only needed if `trusted_connection` is 'no').
- **password**: Your SQL Server password (only needed if `trusted_connection` is 'no').

### OUTPUT Section
- **output_dir**: The directory where the Parquet files will be saved. Default is `parquet_files`.
- **compression**: The compression method used for saving Parquet files. The default is `snappy`, but other options (like `gzip`) are available.

Example configuration:

```ini
[DATABASE]
server = localhost
database = YourDatabase
trusted_connection = yes
username = 
password = 

[OUTPUT]
output_dir = parquet_files
compression = snappy
```

## Installation

Since this is a pre-built executable file, there is no installation required. Simply download the `.exe` file and double-click it to run the application. Ensure you have the necessary Python runtime environment if building the application from source.

## Contributing

This project is open-source, and contributions are welcome! If you encounter issues or have suggestions for improvements, feel free to open an issue or submit a pull request.

## License

This project is open-source and available under the MIT License. Feel free to modify, fork, or distribute it according to your needs.

## Summary

The **SQL to Parquet Converter** provides a simple and efficient way to export SQL Server database tables to Parquet files, which can be useful for further data analysis or storage in big data ecosystems. The application handles large datasets efficiently, allows for custom output settings, and provides detailed logging and error handling.