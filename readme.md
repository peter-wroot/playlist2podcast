# playlist2podcast

A python script to convert a YouTube playlist to an mp3 podcast. Utilises youtube-dl and ffmpeg.

Only tested on windows - should work on Linux/MacOS if you provide youtube-dl and ffmpeg paths.

## Requirements:

Executables:  
* youtube-dl   
* ffmpeg  

Python Modules:
* os
* subprocess
* json
* argparse

## Command-Line Arguments

| Switch    | Usage                                             | Default           |
|-          |-                                                  | -                 |
| `-p`      | URL of YouTube Podcast                            | N/A
| `-t`      | String to embed as the podcast title metadata     | N/A
| `-a`      | String to embed as the podcast artist metadata    | N/A
| `-y`      | Path to youtube-dl executable                     | `youtube-dl.exe` (in script directory)  |
| `-f`      | Path to ffmpeg executable                         | `ffmpeg.exe` (in script directory)      |

## Notes

* Tracks are automatically numbered based on their position in the playlist.
* Artist, podcast title, and track number are embedded into the finished mp3 file.
* track number and track title are set as the file name for easy organization.
* Automatic removal of non-valid characters from the file name.