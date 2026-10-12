# Simple Line Editor in C

## Overview

The Simple Line Editor is a command-line application developed in C. It allows users to create, edit, search, and manage text documents through simple commands.

This project was developed as part of **Activity 7: Build a Simple Line Editor in C**.

## Features

- Insert a line at a specified position
- Delete a line from the document
- Display the complete document with line numbers
- Save document contents to a text file
- Load document contents from a text file
- Search for a word or substring
- Find and replace text
- Undo the previous supported modification
- Count the total number of lines and words
- Display command instructions using `help`

## Technologies Used

- Programming language: C
- Standard libraries: `stdio.h`, `string.h`, `ctype.h`
- Compiler: GCC

## Data Structure

The program uses two-dimensional character arrays to store the document and its backup.

- `doc[MAX][LEN]` stores the current document.
- `old[MAX][LEN]` stores the previous document state for undo.
- `lines` tracks the current number of lines.
- `oldLines` tracks the number of lines in the backup.

The maximum capacity is 100 lines, with a maximum of 199 text characters per line.

## Requirements

- GCC compiler or another compatible C compiler
- Terminal or command prompt
- Windows, Linux, or another environment that supports compiling and running C programs

## Compilation

Compile the source file using GCC:

```bash
gcc line_editor.c -o line_editor
```

On Windows, run the executable using:

```powershell
.\line_editor.exe
```

On Linux, run:

```bash
./line_editor
```

Replace `line_editor.c` with the actual source filename if it differs.

## Usage

Start the program and type:

```text
help
```

This displays the available commands.

### Command Examples

```text
insert 1
display
search Hello
replace Hello Hi
count
save document.txt
load document.txt
delete 1
undo
quit
```

The `insert` command asks for the text after the position is supplied.

## Project Files

- `line_editor.c` — Main C source code
- `README.md` — Project overview, features and usage instructions
- `help.txt` — Detailed command reference
- `document.txt` — Example saved document, created when the save command is used

## Limitations

- The document supports a maximum of 100 lines.
- Each line supports up to 199 text characters.
- The current command interface accepts single-word search and replacement arguments.
- Undo stores one previous document state rather than a complete history of changes.
- The program does not automatically save the document when it exits.

## Conclusion

This project demonstrates basic file handling, string manipulation, arrays, functions, searching, replacing, and command processing in C.

It provides a simple foundation for understanding how a text-based line editor works.

## Author

Developed as part of the Activity 7 C programming project.
