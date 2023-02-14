## Lab 3 Blog Post

## Find Command Options

When using the find command, there are several options available to refine your search. Below are examples of using four options: -delete, -type, -mtime, and -exec.

# -delete

The -delete option removes the files or directories that are found. This option can be dangerous, so use it with caution.

Example 1: Deleting files from ./written_2
```
find ./written_2 -name "*.txt" -delete
```
This command finds all .txt files in the ./written_2 directory and deletes them.

Example 2: Deleting empty directories from ./written_2
```
find ./written_2 -type d -empty -delete
```
This command finds all empty directories in the ./written_2 directory and deletes them.

# -type

The -type option allows you to search for specific types of files, such as directories or regular files.

Example 1: Finding directories in ./written_2
```
find ./written_2 -type d
```
This command finds all directories in the ./written_2 directory.

Example 2: Finding executable files in ./written_2
```
find ./written_2 -type f -perm /u+x
```
This command finds all executable files in the ./written_2 directory.

# -mtime

The -mtime option allows you to search for files based on when they were last modified.

Example 1: Finding files modified within the last 7 days in ./written_2
```
find ./written_2 -type f -mtime -7
```
This command finds all files in the ./written_2 directory that were modified within the last 7 days.

Example 2: Finding files modified between 7 and 14 days ago in ./written_2
```
find ./written_2 -type f -mtime +7 -mtime -14
```
This command finds all files in the ./written_2 directory that were modified between 7 and 14 days ago.

# -exec

The -exec option allows you to execute a command on the files or directories that are found.

Example 1: Changing permissions on all files in ./written_2
```
find ./written_2 -type f -exec chmod 644 {} \;
```
This command finds all files in the ./written_2 directory and changes their permissions to 644.

Example 2: Renaming all .txt files in ./written_2 to .md
```
find ./written_2 -name "*.txt" -exec sh -c 'mv "$0" "${0%.txt}.md"' {} \;
```
This command finds all .txt files in the ./written_2 directory and renames them to .md files.
