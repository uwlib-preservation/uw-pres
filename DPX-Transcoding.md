# DPX transcoding via FFmpeg

## Overview
While UW prefers MKV/FFV1 film preservation files to be created via the [RAWCooked](https://mediaarea.net/RAWcooked) tool by [MediaArea](https://mediaarea.net/), this isn't always possible or practical depending on the nature of the project. In this case, [FFmpeg](https://www.ffmpeg.org/) may be used to compress DPX stacks into the necessary FFV1/Matroska files.

## Command for 10 bit 2k transcode
`ffmpeg -f image2 -start_number NUMBER -r FRAMERATE -report -i IN%08d.dpx -c:v ffv1 -level 3 -slices 16 -slicecrc 1 -g 1 -coder 1 -context 0 -pix_fmt gbrp10le -r FRAMERATE OUT.mkv`

__Notes__:
* `-report` will cause FFmpeg to write a lot to the current directory. It is suggested to run this command from within the project directory.
* `IN%08d` should be changed to reflect the number of digits used in incrementing file numbering. This example uses eight digits.
* FRAMERATE must be consistent across both usages. Can be 18, 23.98, 24 or others as appropriate. __NOTE:__ Using a framerate of 23.98 has been found to make MediaInfo report an incorrect number of total frames in the output MKV, so comparison against number of DPX files may be innacurate using MediaInfo. 
* -f md5 -pix_fmt gbrp10le -r FRAMEMATE OUT.md5 can be added to command to simultaneously generate an MD5 file of original frames to confirm losslessness.
