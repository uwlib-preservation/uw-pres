# UW Libraries Media Reformatting Workflows

### Pre-Digitization Steps
* [Digital Workflows Checklist](https://goo.gl/forms/tdjzjzLR620z00UR2)
* Section 108 Rights Research (When applicable)
  - [Online Form](https://drive.google.com/open?id=1s_xVbNGo2iRcvElfns4HyMztqWp5XdrzErxyLc6dChE)
  - [Media Center Version](https://github.com/pugetsoundandvision/uw-pres/raw/master/media_rights_search_checklist.docx)
  
### Guiding Principles for Preservation Master Files
* All preservation masters should be accurate and true representations of their source materials, and should be complete digital proxies to the extent that is feasible. They must maintain all essential original characteristics, such as (but not limited to) audio track orientation, aspect ratio, frame rate etc.
* All machines should be calibrated for the best possible capture of each item. This includes azimuth adjustment for audio tapes, and the use of a processing amp for video signals.
* Any manipulation, such as audio peak normalization or color correction should be applied in the creation of a reproduction master file (or mezzanine) and not applied to the preservation master file.

### Guiding Principles for Mezzanine/Access Files
All access files should strive to be the truest representation of the intended presentation of the materials as experienced on its original playback equipment. For example:
* Access copies of interlaced material should be deinterlaced as this is how a viewer would have experienced the original media.
* Mono audio files should be converted into dual-mono access files for correct listening experience - audio levels should be normalized if necessary.
* Anamorphic materials should be at their intended viewing aspect ratio.

### Preferred File Formats
#### Audio Formats
Format|Preservation Codec|Preservation Wrapper|Attributes
---|---|---|---
Analog Audio Tape|24 Bit PCM|Broadcast WAVE|96kHz Sample rate
Audio Grooved Media|24 Bit PCM|Broadcast WAVE|96kHz Sample rate
Digital Audio Tape|PCM|Broadcast WAVE|Sample rate/Bit depth same as source
Audio CDs (CD-DA)|16bit PCM or 16 bit FLAC|Broadcast WAVE or FLAC + CUE Sheet|44.1 kHz sample rate
MiniDisc|24 Bit PCM|Broadcast WAVE| 44.1 kHz sample rate

#### Video Formats
Format|Preservation Codec|Preservation Wrapper|Attributes
---|---|---|---
Analog Video Tape|10 bit FFV1 version 3|Matroska (MKV)|Audio should be 24 Bit/48 kHz PCM
DV Tape Family|Same as Source (DV or HDV)|Matroska|DV encoded materials should always be captured natively via Firewire
Digital8|DV|Matroska|DV encoded materials should always be captured natively via Firewire
Other Digital Video Tape|FFV1 version 3|Matroska (MKV)|Audio should be 24 Bit/48 kHz PCM


#### Film Formats
Preservation files for film based formats should be created from DPX with [RAWcooked tool](https://mediaarea.net/RAWcooked)
Format|Preservation Codec|Preservation Wrapper|Attributes
---|---|---|---
35mm Film|16 bit FFV1|Matroska|4k resolution over scan.
16mm Film|10 bit FFV1|Matroska|2k resolution over scan.
8mm Film|10 bit FFV1|Matroska|2k resolution over scan.

### Preferred Naming Conventions
For reformatted materials, UW Libraries prefers file names that are human readable and self descriptive. These names should always provide a clear association between the digital item and its physical source object.

Preservation files created by reformatting projects should adhere to the following naming convention:

`[MARC Code for collecting institution]_[collection #-collection name]_[item number]_[side/part]`

For example:

`wauar_1693-001-jacobs_14580_side1`


#### Naming Instructions:
* There should be __no__ spaces or special charaters in file names. Only standard letters and numbers should be used, with the exception of dashes and underscores.
* Underscores must __only__ be used to separate components of the file name as shown above.
* [MARC Code for collecting institution] will always be  wauar for items housed in UW Special Collections.
* [collection #-collection name] Collection number and an abbreviated collection name must be included and separated by a ‘-’. The abbreviated name can be as simple as one word.
* An item number must be included in file name. This should take the form of the most accurate number that has been assigned to the item. (If a catalog number exists it should be used). Examples are:
  * `Box1-Tape1`
  * `99320152284601451`
* If desired a more descriptive title can be added to the item number by separating with a dash. [Camel Case](https://en.wikipedia.org/wiki/Camel_case) is preferred for multi-word titles. Example:
  * `14-003-windowsOnTheWorld`
* [side/part] Sides should be included in filenames when applicable. This should be written as Side1, Side2 etc. If there are multiple regions on the same side that must be split into separate files (such as speed changes mid tape) these should be noted with the addition of lowercase letters. If sides are not relevant to the media, or if there is only a single informational side with multiple regions 'part' should be used. Examples: 
  * `Side1a, Side1b, Side2`
  * `Part1, Part2`
* If there is only a single side with a single region, side information does not need to be noted.
### Expected Deliverables
* Preservation File
* Mezzanine File
* Access File
* Picture(s) of original item
* MD5 Checksums for all files

### Post-Migration Quality Control
* [Audio QC Script](https://github.com/pugetsoundandvision/uwmediascripts/blob/master/audioqc)
* [QC Tools](https://mediaarea.net/QCTools) for video in combination with spot checks
* Spot checks of random sample
* Optional in house capture comparison as needed


### Additional Links
* [MDPI FFV1 White Paper](https://mdpi.iu.edu/doc/MDPIwhitepaper.pdf)
### LoC Links
* [24 Bit LPCM](https://www.loc.gov/preservation/digital/formats/fdd/fdd000011.shtml)
* [Broadcast WAVE](https://www.loc.gov/preservation/digital/formats/fdd/fdd000003.shtml)
* [DV](https://www.loc.gov/preservation/digital/formats/fdd/fdd000183.shtml)
* [FLAC](https://www.loc.gov/preservation/digital/formats/fdd/fdd000198.shtml)
* [FFV1](https://www.loc.gov/preservation/digital/formats/fdd/fdd000341.shtml)
* [Matroska](https://www.loc.gov/preservation/digital/formats/fdd/fdd000342.shtml)
