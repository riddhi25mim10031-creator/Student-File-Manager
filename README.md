# Student-File-Manager
# Student File Manager

A simple command-line Student File Manager written in Python that performs basic CRUD operations (Create, Read, Update, Delete) on a CSV file. The program stores student records (Roll, Name, Class, Marks) in `student_data.csv` and provides a text-based menu for interacting with the data.

## Project Overview

This is a lightweight CLI application intended for learning purposes and small local usage. It demonstrates file I/O with CSV, basic data validation (duplicate roll-number prevention), and simple record management using standard Python libraries.

Key behaviors:
- Automatically creates `student_data.csv` with a header row if it doesn't exist.
- Supports adding new student records, viewing a list of students, searching by roll number, updating a student's record, and deleting a student record.
- All data is stored as CSV text in the repository directory.

## Features

- Add student (Roll, Name, Class, Marks) with duplicate roll number check
- Display all student records in a formatted table
- Search for a student by Roll number
- Update an existing student's details
- Delete a student record
- Automatic CSV file initialization

## Technologies / Tools Used

- Python 3 (recommended)
- Standard library modules:
  - csv
  - os
- Terminal / command prompt

No external dependencies are required.

## File created / used

- `student_data.csv` — created at runtime if missing; stores records in the format:
  Roll,Name,Class,Marks

- The Python script (example filename used in instructions below) contains the program logic and CLI menu.

## Installation and Setup

1. Ensure Python 3 is installed:
   - Check with `python3 --version` or `python --version`.

2. Clone the repository (replace with your fork URL if needed):
   ```bash
   git clone https://github.com/riddhi25mim10031-creator/Student-File-Manager.git
   cd Student-File-Manager
   ```

3. (Optional) Create a virtual environment:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate      # macOS / Linux
   .venv\Scripts\activate         # Windows
   ```

4. Run the program:
   - If the script file is named `student_manager.py` (or similar), run:
     ```bash
     python3 student_manager.py
     ```
   - If your Python is `python` on your system:
     ```bash
     python student_manager.py
     ```

Note: If your script has a different filename, replace `student_manager.py` above with the actual filename (for example, `main.py`).

## Usage

When you run the script, a menu is displayed:

```
1. Add
2. Update
3. Delete
4. Search
5. Display
6. Exit
```

- Choose the option number and follow on-screen prompts.
- The program will create `student_data.csv` automatically if not present.

Example session:
- Add -> Enter Roll No: 101 -> Name: Alice -> Class: 10 -> Marks: 95
- Display -> shows a table with the student record
- Search -> Enter Roll No: 101 -> shows "Found"
- Update -> Roll No to change: 101 -> enter new values -> Updated.
- Delete -> Roll No to delete: 101 -> Deleted.

## CSV Format Example

The CSV file will look like:

```
Roll,Name,Class,Marks
101,Alice,10,95
102,Bob,9,88
```

## Instructions for Testing

Manual testing steps:
1. Start with a fresh repository directory (or delete `student_data.csv` to start fresh).
2. Run the script.
3. Test each menu option in this order:
   - Add a student (try adding two students).
   - Attempt to add a student with an existing Roll No to confirm duplicate prevention.
   - Display all students and verify the output format.
   - Search for an existing and a non-existing Roll No.
   - Update a student's Name/Class/Marks and verify by Display or Search.
   - Delete a student and verify the record is removed.
4. Try edge cases:
   - Provide empty inputs for some fields and see the behavior.
   - Try non-numeric Marks (the program currently stores whatever you input).
   - Check behavior when `student_data.csv` is missing or has been corrupted.


