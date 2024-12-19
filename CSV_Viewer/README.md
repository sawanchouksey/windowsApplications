# CSV Viewer Application

This application allows you to view large CSV files in chunks, making it ideal for handling files of any size, without the need for advanced memory management. The CSV Viewer App provides an intuitive interface to navigate through large datasets efficiently, allowing users to load and view data in smaller, manageable chunks.

## Key Features:
- **Open CSV Files:** Easily select and open any CSV file using a file dialog.
- **Chunk Navigation:** View CSV data in chunks (default size of 10,000 rows), with navigation buttons to move between chunks.
- **Scroll Support:** Vertical and horizontal scrollbars to navigate through the data.
- **Efficient Memory Usage:** Loads data in chunks, preventing large files from overwhelming system memory.
- **NULL Handling:** Missing values in the CSV are displayed as `NULL`.
- **User-Friendly Interface:** Simple, intuitive interface for smooth user experience.

## Technology Stack

This application is built using the following technologies:

1. **Python** – The main programming language for this application.
2. **Pandas** – Used for handling and reading large CSV files in chunks. The `read_csv` function with `chunksize` ensures that only a portion of the file is loaded into memory at any time.
3. **Tkinter** – A standard Python library for creating graphical user interfaces (GUIs). It is used to create the application window, display the CSV data in a table, and provide interactive buttons and scrollbars.
4. **ttk (Themed Tkinter Widgets)** – Used for adding styled widgets, such as the `Treeview` for displaying tabular data and scrollbars.

## How to Use

1. **Launch the Application:**
   - Open the executable file and the main window will appear.

2. **Open a CSV File:**
   - Click the **Open CSV File** button and select a CSV file to view.

3. **Navigate Through the Data:**
   - Use the **Previous Chunk** and **Next Chunk** buttons to load and view data in chunks.
   - The chunk index will be displayed to show the current chunk number.

4. **Scroll Through Data:**
   - You can use the vertical and horizontal scrollbars to navigate through the displayed data.

5. **View NULL Values:**
   - Missing or empty cells in the CSV will be displayed as `NULL` for clarity.

## Installation

Since this is a pre-built executable file, there is no installation required. Simply download the `.exe` file and double-click it to run the application. Ensure you have the necessary Python runtime environment if building the application from source.

## Requirements

If you want to run or modify the source code yourself, make sure you have the following Python libraries installed:

- **pandas** – To install: `pip install pandas`
- **tkinter** – This is included with Python, so no need to install separately.

## License

This project is open-source and available under the MIT License. Feel free to contribute, fork, or modify it as needed.

## Troubleshooting

- **File Not Opening**: If the file fails to load, ensure the CSV file is properly formatted and not corrupted.
- **Navigating Back**: You cannot navigate to the previous chunk if you're already at the beginning of the file. A message will inform you when this happens.

## Contributing

If you have suggestions for improvements or bug fixes, feel free to open an issue or submit a pull request. Contributions are welcome!

## Conclusion

This CSV Viewer Application provides a simple and efficient way to view large CSV files without any memory constraints, allowing users to easily navigate through chunks of data and manage files of virtually any size.

### Support Me

**If you find my content useful or enjoy what I do, you can support me by buying me a coffee. Your support helps keep this website running and encourages me to create more content.**

[![Buy Me a Coffee](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/sawanchokso)

**Your generosity is greatly appreciated!**

##### Thank you for your support!💚
