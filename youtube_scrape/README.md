# youtube_scrape
Internal library for scraping youtube videos. Alternative to pafy, pytube, and youtube-dl. 

Insert the youtube playlist name and url and download to folder. Then, convert all videos to .mp4 format for further processing.

This is good for emotional labels (angry, happy, sad, etc.) to be further processed, or just any video with sounds that we'd like to look further into. 

## making playlists

To make a playlist:
    
    cd ~
    git clone git@github.com:NeuroLexDiagnostics/tribe3_emotions.git
    cd tribe3_emotions/youtube_scrape 
    python3 make_playlist.py
    what is the playlist id?
    ...

This then makes a playlist from all the playlist ids. Note that only the first 100 in each playlist will be added to the playlist. Also, don't worry about duplicate video links in similar playlists (e.g. cnn videos); we take care of this by making sure no duplicate links go into the playlist. 

Note that you can search by playlist in youtube. Also, the playlist id is the id part of the URL (https://www.youtube.com/watch?v=ZqZ3CwQqeNc&list=PLA64498EB9B1CBF95, PLA64498EB9B1CBF95 = playlist ID).

## downloading playlists generated 

Once you make a playlist, you can easily download it by:

    cd ~ 
    cd train_emotions/youtube_scrape
    python3 download_playlist.py 
    
This will then download the playlist and format it according to the style needed to train emotion detection models with train_emotions library.
 
 ## references
 * [pytube](https://github.com/nficano/pytube)
