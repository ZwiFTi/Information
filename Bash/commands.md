Print: echo 'foo'
List directories: ls
Which directory am i in?: pwd (printWorkingDirectory)
Move item: mv
remove file: rm file.txt
remove dir: rmdir directory



# List all items in directory that is of type .pdf:

`ls -l Documents/*.pdf`

# Move many items of a similar sort into a folder:

`mv Documents/*.pdf Documents/ebooks`

# download file from web:

curl -L -o dictionary.txt 'https://tinyurls.com/zeyg9vc'


# Read a file (less)

less dictionary.txt
space: scroll down
arrow keys: scroll one at a time
B: back
slash: search
Q: quit

# The best search function:

grep findThisWord file.txt

This will read the file and output all the lines that contain that word

more:

curl -L https://tinyurl.com/zeyq9vc | grep fish
