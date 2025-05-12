# Metadata fingerprinting attack

Demonstrates extracting identifying metadata from documents:

```python
from PIL import Image
import exifread
import os

def extract_metadata(file_path):
    if file_path.lower().endswith(('.png', '.jpg', '.jpeg')):
        with open(file_path, 'rb') as f:
            tags = exifread.process_file(f)
            print("=== Image Metadata ===")
            for tag in tags:
                if tag not in ('JPEGThumbnail', 'TIFFThumbnail'):
                    print(f"{tag}: {tags[tag]}")
    
    # PDF metadata extraction
    elif file_path.lower().endswith('.pdf'):
        from PyPDF2 import PdfFileReader
        with open(file_path, 'rb') as f:
            pdf = PdfFileReader(f)
            info = pdf.getDocumentInfo()
            print("\n=== PDF Metadata ===")
            for key in info:
                print(f"{key[1:]}: {info[key]}")
```