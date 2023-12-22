# Office Scripts

## plus

The "plus" script is designed to enhance the formatting of phone numbers in CSV files by adding the '+' symbol.

The program follows specific rules to determine how the plus symbol is added.

Additionally, it's important to note that if a phone number does not match any of the specified formats, the entire line will not be recorded, potentially resulting in data loss.

### Formating

Formatting Rules:
- Rule 1: If the number starts with '9' and has a length of 10 digits, the script adds '+7' to the beginning of the number.
- Rule 2: If the number starts with '79' and has a length of 11 digits, the script adds a single '+' to the beginning of the number.
- Rule 3: If the number starts with '+79' and has a length of 12 digits, no changes are made to the number.
- Rule 4: If the number starts with '89' and has a length of 11 digits, the script adds '+7' to the number, excluding the leading '8'.

Handling Unmatched Numbers:
If a phone number in the CSV file does not adhere to any of the specified formatting rules,
the entire line containing that number will be excluded from the processed output.

**This means that if certain numbers do not fit the expected formats, those particular lines will not be saved, potentially leading to data loss.**

#### Recommendations:
- Data Validation: Ensure that the input CSV file primarily contains phone numbers that adhere to the specified formatting rules.
- Backup: Prior to running the script, consider creating backup copies of your CSV files to mitigate the risk of unintentional data loss.

### Key Features:
- File Selection Flexibility: The program supports the use of wildcards (* and ?) for selecting multiple files.
- Configurability: Ability to specify the column index and CSV delimiter through command line arguments.
- Efficiency: Processes multiple files simultaneously for accelerated batch contact processing.

## minus

The "minus" script is designed to modify the formatting of phone numbers in CSV files by removing the '+' symbol. This script is useful for standardizing phone number formats.

### Formatting Rules:
- Rule 1: If the number starts with '+79' and has a length of 12 digits, the script removes the leading '+'.
- Rule 2: If the number starts with '79' and has a length of 11 digits, the script removes the leading '+'.
- Rule 3: If the number starts with '9' and has a length of 10 digits, the script keeps the number as is.

Handling Unmatched Numbers:
If a phone number in the CSV file does not match any of the specified formatting rules, it remains unchanged.

Note:
The script does not exclude entire lines; instead, it selectively removes the leading '+' from eligible numbers.

## merge

The "merge" script facilitates the merging of CSV and Excel files based on a specified field. It utilizes the pandas library to read, merge, and save dataframes.
Key Features:

File Format Flexibility: Supports both CSV and Excel file formats for input files.

### Usage Instructions:
1. Navigate to the Script Directory:
Open a terminal or command prompt and navigate to the directory containing the "merge.py" script.
2. Run the Script:
Execute the script using the following command template:
```bash
python merge.py <file1_path> <file2_path> [--on FIELD] [--output OUTPUT_FILE] [--encoding ENCODING] [--how {inner, outer, left, right}]
```

Optional Arguments:
--on FIELD: Specify the field to merge on (default: "Телефон").

--output OUTPUT_FILE: Specify the output file name (default: merged_file.csv).

--encoding ENCODING: Specify the encoding for CSV files (default: Windows-1251).

--how {inner, outer, left, right}: Specify the type of merge (default: inner).

## intersec 


## failcalls

## rmbil

## vcard

## vct
