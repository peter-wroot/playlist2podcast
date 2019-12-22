# playlist2podcast

A python script to convert a YouTube playlist to an mp3 podcast. Utilises youtube-dl and ffmpeg.

Tested on MacOS and Windows - should work on Linux too.

## Requirements:

Executables:  
* youtube-dl   
* ffmpeg  

Python Modules:
* os
* subprocess
* json
* argparse
* tempfile
* pathlib

## Command-Line Arguments

| Switch    | Usage                                             | Default                   |
|-          |-                                                  | -                         |
| `-p`      | URL of YouTube Podcast                            | N/A                       |
| `-t`      | String to embed as the podcast title metadata     | N/A                       |
| `-a`      | String to embed as the podcast artist metadata    | N/A                       |
| `-y`      | Path to youtube-dl executable                     | `youtube-dl` (in path)    |
| `-f`      | Path to ffmpeg executable                         | `ffmpeg` (in path)        |
| `-o`      | Path to save finished audio files                 | User's home folder        |

## Example

`python playlist2podcast.py -p https://www.youtube.com/playlist?list=PL0CFk33kNHvSdeJm6HQtiJygOCV0o9JdK -t "Citation Needed"
-a "The Technical Difficulties"`

## Notes

* Tracks are automatically numbered based on their position in the playlist.
* Artist, podcast title, and track number are embedded into the finished mp3 file.
* track number and track title are set as the file name for easy organization.
* Automatic sanitization of non-valid characters from the file name.
* Creates directory structure for Podcast Author / Podcast title 