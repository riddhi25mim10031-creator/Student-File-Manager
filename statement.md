# Student Records Manager — Project Statement

## Project Statement
Student Records Manager is a simple command-line application that provides basic CRUD (Create, Read, Update, Delete) operations for managing student records stored in a CSV file (student_data.csv). The tool enables adding new students, preventing duplicate roll numbers, listing all records, searching by roll number, updating existing records, and deleting records — all from a lightweight, portable command-line interface.

## Scope of the Project
In scope:
- Storing student records in a CSV file (student_data.csv).
- Initializing the CSV file with a header if it does not exist.
- Adding new student records with duplicate roll-number checks.
- Viewing a formatted list of all students.
- Searching for a student by roll number.
- Updating a student's name, class, and marks by roll number.
- Deleting a student record by roll number.
- Simple, interactive text-based CLI menu for user interaction.

Out of scope (for this version):
- Authentication, user roles, or access control.
- Concurrency control for simultaneous access by multiple processes/users.
- Advanced validation or type-checking for fields (e.g., numeric-only marks).
- Import/export beyond the CSV file, database persistence, or GUI/web interfaces.
- Encryption, backups, or automated versioning of the CSV file.

## Target Users
- Teachers and instructors who need a small, local tool to track student roll numbers, names, classes, and marks.
- Students learning basic Python file I/O and CSV handling who want an example CRUD application.
- Small-scale projects or scripts where a full database would be unnecessary overhead.

## High-Level Features
- Initialization
  - Automatically creates `student_data.csv` with header row when the program first runs.
- Add Student
  - Prompt for Roll, Name, Class, and Marks.
  - Detects and prevents duplicate Roll numbers.
  - Appends new records to the CSV.
- View / Display
  - Reads the CSV and prints a neatly formatted table of records (skips header when appropriate).
  - Handles empty/no-record conditions gracefully.
- Search
  - Lookup by Roll number and show matching student details.
- Update
  - Replace an existing student's Name, Class, and Marks by matching Roll number.
  - Writes updated data back to the CSV atomically (read all, modify, then write).
- Delete
  - Remove a student's record by Roll number and rewrite the CSV without the deleted record.
- CLI Menu
  - Repeated interactive menu with options for Add, Update, Delete, Search, Display, and Exit.

## Non-functional Considerations
- Simplicity: Minimal dependencies (only Python standard library csv and os).
- Portability: Works on any environment with Python installed and write access to the working directory.
- Transparency: Data stored in a plain CSV file for easy inspection and manual edits.
- Usability: Interactive text prompts aimed at non-technical users comfortable with terminal/console.

## Assumptions & Limitations
- The Roll number is treated as the unique identifier and compared as a string.
- The program assumes a single-user environment; concurrent edits may cause data loss.
- No strict validation of input types (e.g., class or marks may be non-numeric strings).
- Error handling is basic; file errors are reported via simple messages rather than structured exceptions.

## Future Enhancements
- Add input validation (enforce numeric marks, valid roll formats).
- Add backup/versioning and simple concurrency handling (file locking).
- Add import/export to other formats (JSON, SQLite).
- Build a simple GUI or web interface for easier use.
- Add sorting, filtering, and bulk operations (batch import/export).
- Add unit tests and improved error reporting.

## Usage (quick)
1. Run the script: python <script_name>.py
2. Use the menu to add, update, delete, search, or display student records.
3. The data is stored in `student_data.csv` in the script's working directory.

## File(s) of interest
- student_data.csv — the CSV file created and used to persist records.
- The main script — contains functions: init, add, view, search, update, delete, main.
