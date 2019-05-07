# clipboard copy


- [STACKOVERFLOW](https://stackoverflow.com/a/5130969/6272061)

```bash
# install program
sudo apt-get install xclip

# paste content to global clipboard!
# include -selection c
echo "clipboard content" | xclip -selection c

# past to "local"/"temp" clipboard
echo "hello worl!" >> file.txt
cat file.txt | xclip
xclip -o # => "hello world"

# maybe a usefull alias?
alias cb="xclip -selection c"
```
