# Searching (Find)

```bash
# findet alle jggs (überall), gibt metadaten aus und wählt nur das Feld "JFIF Version" aus!
find . -iname '*jpg' -exec exiftool {} \; | egrep "JFIF Version"
```