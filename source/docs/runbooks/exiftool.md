# Cleaning metadata with ExifTool

For thorough metadata removal, ExifTool is the most capable option. It needs [installing](https://exiftool.sourceforge.net/install.html) first; after that, everything runs from a terminal or command prompt.

To clean a single file:

```bash
exiftool -all= -overwrite_original yourfile.jpg
```

To clean every file in a folder:

```bash
exiftool -all= -overwrite_original /path/to/folder/
```

This permanently removes the hidden data from the files.
