# Metadata fingerprinting

A photograph taken on a modern smartphone contains far more than the image. Embedded in the file is a structured record: the camera model, lens settings, time of capture, GPS coordinates if location services were enabled, and sometimes a thumbnail of the image as it appeared on screen. Documents created in office software carry their own records: the author's name as registered in the application, the organisation, revision history, the time of creation and last modification, and occasionally comments or earlier drafts believed to have been deleted.

The attack is passive and requires no exploitation. The metadata is present in the file by design, preserved by default, and visible to anyone who reads the file with appropriate tools.

## How it works

An extraction script opens the file, reads the embedded metadata block, and prints its contents. The logic differs slightly by file type but follows the same structure.

```
open file

if file is an image (JPEG, PNG):
    read EXIF block
    extract:
        GPS latitude and longitude    → precise location
        device model and manufacturer → narrows the population of likely senders
        timestamp                      → date, time, sometimes timezone
        camera settings               → aperture, shutter speed, ISO

if file is a PDF or office document:
    read document metadata block
    extract:
        author name and organisation
        creation date and last-modified date
        revision count and editing time
        software version used to create it
    check revision history:
        may contain deleted paragraphs or earlier versions of text
```

The GPS coordinates embedded in an image taken with location services enabled give the exact spot where the photograph was taken, to within a few metres. Combined with the timestamp, they place a specific person at a specific place at a specific time. The device model, combined with other information, can narrow down the population of people who might have taken the photograph considerably.

## What this reveals

Documents released publicly by organisations or individuals have repeatedly revealed their authors through metadata that was never noticed before publication. A 2003 example involved a United Kingdom government dossier on Iraqi weapons: the document's revision history showed the names of several individuals who had contributed to its drafting, information the government had not intended to disclose. Similar incidents recur regularly, in legal filings, in leaked documents, in photographs shared without attention to what they carry.

The metadata travels with the file everywhere it goes, through sharing, through forwarding, through publication. Removing it requires a deliberate extra step.

## Defences

Several free tools read and strip metadata from common file types. For images, tools such as ExifTool can remove the EXIF block entirely or overwrite specific fields. For documents, most office applications offer a "remove personal information" option before saving. Making this a habit before sharing files outside a household or organisation is straightforward once the step is part of the workflow.

The more fundamental defence is disabling location services for the camera application on a smartphone. If GPS coordinates are never written into the file in the first place, they cannot be extracted from it later.
