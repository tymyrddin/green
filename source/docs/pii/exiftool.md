# The most thorough cleaning method (using ExifTool)

For complete removal of metadata, ExifTool is the most powerful option. First, you'll need to 
[install it](https://exiftool.org/install.html) on your computer. Once installed, open your terminal or command prompt.

To clean a single file, type:

```bash
exiftool -all= -overwrite_original yourfile.jpg
```

To clean all files in a folder:

```bash
exiftool -all= -overwrite_original /path/to/folder/
```

This will permanently remove all hidden data from your files.