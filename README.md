# PlexGifMaker
A quick way to make GIFs using your Plex Library and Subtitles.  

Integrated Plex Login. Docker-Compose build.  Written in C#/.NET 6.0.  

The only thing you need is your Plex URL. 
![PlexGifMakerDemo](https://github.com/TechBuckler/PlexGifMaker/assets/166867994/f57dad0a-1004-4d45-a871-fc212b2078c0)
Only runs on http for now.  Port 9000.

# Installation

Clone the repository and run the commands below

```
cd PlexGifMaker/PlexGifMaker
docker build --network host -t plexgifmaker .
docker compose up
```
The --network host addition was necessary for this to work as the default docker compose --build was not working on my systems. The extra folder is a bug from the upstream, make sure you are in the folder with the Dockerfile before running the docker build command.

# Known Issues

This works great with SDR content, but HDR content isn't handled properly as tone mapping is not being done by the ffmpeg commands.
