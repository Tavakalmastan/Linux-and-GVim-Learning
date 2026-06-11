Day 05 - File Searching, Comparison and Text Statistics

Objective

Learned how to search files and directories, compare files using different Linux utilities, and analyze file contents using counting commands.

Topics Covered
1. find Command

The find command is used to search for files and directories recursively based on different conditions.

Common Usage
find . -name "*.txt"
find . -type f
find . -type d
find . -size +100M
find . -mtime -7
find . -perm 644
Key Learnings
Search files by name
Search only files or directories
Search based on size
Search based on modification time
Search based on permissions
Execute commands on search results
2. File Comparison Commands

Linux provides multiple utilities to compare files and identify differences.

diff

Compares files line by line.

diff file1.txt file2.txt
diff -u file1.txt file2.txt
diff -y file1.txt file2.txt
cmp

Compares files byte by byte.

cmp file1.txt file2.txt
cmp -l file1.txt file2.txt
cmp -s file1.txt file2.txt
comm

Compares two sorted files.

comm file1.txt file2.txt
comm -1 file1.txt file2.txt
comm -2 file1.txt file2.txt
comm -3 file1.txt file2.txt
Key Learnings
diff shows line-level differences.
cmp shows byte-level differences.
comm compares sorted files and displays common and unique lines.
3. wc Command

The wc command is used to count lines, words, characters, and bytes.

Common Usage
wc file.txt
wc -l file.txt
wc -w file.txt
wc -c file.txt
wc -m file.txt
wc -L file.txt
Key Learnings
Count total lines in a file
Count total words
Count characters and bytes
Find the longest line length
Useful for log files and reports
