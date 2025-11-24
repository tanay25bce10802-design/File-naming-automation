File-Naming Automation Tool

A command-line utility for automated, customizable, and robust batch file renaming—especially helpful for organizing chronologically sensitive files like photographs and documents. Built with Python, this tool streamlines large-scale file management by extracting file metadata and embedding it into filenames in a human-readable, consistent format.​

Features
Date-Based Renaming: Rename files using their creation or last modification timestamp.

Customizable Templates: Specify custom date/time formats using Python’s strftime directives.

Prefix/Suffix: Add optional prefixes and suffixes to filenames.

Conflict Handling: Automatically resolve name conflicts by appending counters.

Directory-Aware: Skips folders when renaming.

Command-Line Interface: Fully functional CLI using argparse for intuitive usage and help messages.​

Requirements
Python 3.x

Libraries: os, argparse, datetime (all standard Python modules)​

Usage
bash

python tool.py date -f <folder_path> -df <date_format> [-p <prefix>] [-s <suffix>] [-m]

-f <folder_path>: Directory containing files to rename

-df <date_format>: Date/time format (e.g., %Y%m%d_%H%M%S)

-p <prefix>: Optional prefix for filenames

-s <suffix>: Optional suffix for filenames

-m: Use last modification time instead of creation time

Examples:

bash

python tool.py date -f ./photos -df "%Y-%m-%d_%H-%M-%S"

python tool.py date -f ./docs -df "%Y%m%d" -p "project" -s "final" -m

Functional Overview
Requirement	Description
Date-Based Renaming	Uses file metadata timestamps to rename files​
Custom Formats	User-defined date/time strings​
Conflict Resolution	Appends counters for duplicate names​
CLI Only	All options available via command line​
Testing & Robustness
Unit and integration tests recommended, including handling edge cases and error states.

Defensive programming ensures files are not accidentally overwritten and permission errors are handled gracefully.​

Extensibility
Future plans include:

Sequential/Replace modes

Recursive folder support

Filetype filtering

Preview/dry-run feature​

Learnings
Efficient use of argparse for multi-mode CLI tools

Practical file metadata handling with os and datetime

Defensive programming and robust error handling​

References
Python 3 official documentation (os, datetime, argparse)​

Author: Tanay Shrivastava

Date: 24th November 2025
