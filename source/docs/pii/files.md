# Removing metadata from files

## The Problem with Windows' built-in metadata removal

The "Remove Properties and Personal Information" feature in Windows has significant limitations that make it inadequate for proper privacy protection:

1. **Limited File Format Support**: Only works with 11 file formats including old Office 2003 files (DOC/XLS/PPT), JPEG, TIFF, PNG, XPS, MP3, MP4, MOV, and ASF/WMA/WMV .

2. **Incomplete Metadata Removal**: Even for supported formats, many metadata elements remain:
   - Office files retain editing time, template info, creation/modification dates, comments, tracked changes, and hidden content 
   - Images keep most EXIF data (including thumbnails), XMP/IPTC data, and camera serial numbers 
   - TIFF files appear cleaned but metadata remains recoverable with a hex editor 

3. **Misleading Interface**: The option "Create a copy with all possible properties removed" only removes what the feature supports, not all metadata the file may contain .

## Better solutions for metadata removal

### For PDF files

While ExifTool can modify PDF metadata, it doesn't permanently remove it - the original data remains recoverable . A more thorough approach involves:

1. First use ExifTool to clear metadata:

```bash
exiftool -all:all= file.pdf
```

2. Then use qpdf to linearize the file and remove orphaned data:

```bash
qpdf --linearize file.pdf clean_file.pdf
```

This combination makes the changes irreversible . However, note this doesn't clean metadata from embedded objects within the PDF .

### For Office documents

Microsoft Office includes a "Document Inspector" that does a decent job for single files, though it lacks batch processing capability . For batch processing Office files, third-party tools like BatchPurifier™ are recommended as they support:
- Multiple Office formats (DOCX, XLSX, PPTX)
- Removal of comments, tracked changes, hidden text, and other sensitive elements 

### For images and other files

ExifTool remains a powerful option for many file types, supporting:

- Over 60 types of hidden data/metadata removal
- Batch processing capabilities
- Support for JPEG, PNG, WebP, SVG, AVI, WAV, MP3, MP4 and more 

## Key recommendations

1. **Don't rely solely on Windows' built-in tool** - it provides a false sense of security 

2. **Use format-specific tools**:
   - Office: Document Inspector or BatchPurifier™
   - PDF: ExifTool + qpdf combination
   - Images: ExifTool or dedicated image cleaners

3. **Consider document conversion**:
   - Converting to PDF via LibreOffice can remove much hidden data
   - For images, consider resaving or taking screenshots

4. **Verify cleaning results** - always check files after cleaning to ensure sensitive data was actually removed

The white paper from [Digital Confidence](https://digitalconfidence.com/Remove-Properties-and-Personal-Information-a-Misleading-Feature.html) provides excellent technical details about Windows' metadata removal limitations, while [ExifTool](https://exiftool.org/)'s documentation explains its PDF handling constraints. For comprehensive cleaning, [specialized tools](https://cyberrunner.medium.com/removing-metadata-from-pdf-files-using-exiftool-and-qpdf-20090b75d7f0) designed specifically for privacy protection are often necessary.