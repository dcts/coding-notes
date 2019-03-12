# Manipulating Files

```bash
# creating files / folders
mkdir folder              # create folder in current working directory
touch file.txt            # create file

# renaming / moving around / adding content
mv file.txt Newname       # rename file
mv file.txt relativePath  # move file to another directory
echo "test" >> fileName   # writes content (string "test") to file
cat file.txt              # show content of file in console
cat > file.txt            # enters writing mode and OVERWRITES or CREATS file
                          # end writing mode by pressing CTRL+Z
# deleting                          
rm -r foldername          # remove folder
rm file.txt               # remove file

# copying
cp <source> <target>      # copy source file to target
cp file file_copy         # copies "file" to "file_copy" in current directory
```
