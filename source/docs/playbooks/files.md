# Removing metadata from files

Documents and images carry hidden information about who made them, when, on what device, and sometimes where. Removing it before sharing a file is a small habit worth having, but the built-in tools people reach for first are often not enough.

## Why the Windows built-in tool falls short

The "Remove Properties and Personal Information" option in Windows is the one most people reach for, and it leaves more behind than it suggests. It handles only a short list of formats, mostly the older Office types (DOC, XLS, PPT), plus JPEG, TIFF, PNG, XPS, and a few audio and video containers. Even for those, plenty survives: Office files keep editing time, template details, revision dates, comments, and tracked changes; images keep most of their EXIF block, embedded thumbnails, and camera serial numbers; and a TIFF that looks clean can still yield metadata to a hex editor. The option labelled "Create a copy with all possible properties removed" removes only what the feature understands, not everything the file holds, which is where the false sense of security comes from.

## PDF files

ExifTool can edit PDF metadata, but on its own it leaves the original values recoverable inside the file. A more thorough approach is two steps. First clear the metadata:

```bash
exiftool -all:all= file.pdf
```

Then rewrite the file with qpdf, which drops the orphaned data left behind:

```bash
qpdf --linearize file.pdf clean_file.pdf
```

Together these make the change stick. Metadata inside embedded objects can still survive, so a genuinely sensitive PDF is often better rebuilt from a clean export than scrubbed.

## Office documents

Microsoft Office includes a Document Inspector that does a reasonable job on a single file. It does not batch-process, so a folder of documents is slow going by hand; a dedicated metadata-removal tool covers that case, at the cost of trusting a third party with the files. Whichever route, the things worth confirming are gone are comments, tracked changes, hidden text, and revision history.

## Images and other files

For images and a wide range of other formats, ExifTool remains the most capable option, covering dozens of metadata types across JPEG, PNG, WebP, SVG, and common audio and video containers, with batch processing. The [ExifTool runbook](../runbooks/exiftool.md) covers the commands.

## A few habits that help

Relying on one built-in tool tends to leave gaps, so it helps to match the tool to the format: Document Inspector or a dedicated cleaner for Office, ExifTool with qpdf for PDF, ExifTool for images. Converting a document to PDF through LibreOffice sheds a good deal of hidden data along the way, and for an image, resaving it or taking a screenshot drops the original metadata. Whatever the method, checking the file afterwards is the step that catches what was missed.

The [Digital Confidence white paper](https://digitalconfidence.com/Remove-Properties-and-Personal-Information-a-Misleading-Feature.html) sets out the Windows tool's limits in technical detail, and [ExifTool](https://exiftool.org/) documents its own PDF handling.

Last reviewed: 2026-07-08.
