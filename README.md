# audible-flatten-chapters
A command line tool that converts the hierarchical chapters created by [audible-cli](https://github.com/mkb79/audible-cli) to a flat format that is understandable to [AAXtoMP3](https://github.com/KrumpetPirate/AAXtoMP3/). It solves the problem where AAXtoMP3 only generates very short audio files containing the titles of sections while the actual content is missing.

## Installation
1. Install [Bun](https://bun.sh/) (`curl -fsSL https://bun.sh/install | bash`)
2. Copy the `audible-flatten-chapters` to your PATH

## Usage
1. `audible download --aaxc --cover --cover-size 1215 --chapter --all`
2. `audible-flatten-chapters`
3. `AAXtoMP3 -e:mp3 -c -D 'MP3/$title \($narrator\)' --use-audible-cli-data *.aaxc`
