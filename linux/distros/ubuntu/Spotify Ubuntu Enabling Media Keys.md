Spotify Ubuntu Enabling Media Keys


# Title: Ubuntu Enabling Media Keys for Spotify

# Reference: https://fabianlee.org/2016/05/25/ubuntu-enabling-media-keys-for-spotify/

# If the keyboard media keys do not work from your Ubuntu desktop, you can use D-Bus support to send the proper commands to Spotify.
# Validate the following commands from the console:

# Play/Pause
- dbus-send --print-reply --dest=org.mpris.MediaPlayer2.spotify /org/mpris/MediaPlayer2 org.mpris.MediaPlayer2.Player.PlayPause

# Next
- dbus-send --print-reply --dest=org.mpris.MediaPlayer2.spotify /org/mpris/MediaPlayer2 org.mpris.MediaPlayer2.Player.Next

# Previous
- dbus-send --print-reply --dest=org.mpris.MediaPlayer2.spotify /org/mpris/MediaPlayer2 org.mpris.MediaPlayer2.Player.Previous

# Then add following custom shourtcuts that runs command above:

#      Name: spotify-play
# Command: dbus-send --print-reply --dest=org.mpris.MediaPlayer2.spotify /org/mpris/MediaPlayer2 org.mpris.MediaPlayer2.Player.PlayPause

#      Name: spotify-next
# Command: dbus-send --print-reply --dest=org.mpris.MediaPlayer2.spotify /org/mpris/MediaPlayer2 org.mpris.MediaPlayer2.Player.Next

#      Name: spotify-prev
# Command: dbus-send --print-reply --dest=org.mpris.MediaPlayer2.spotify /org/mpris/MediaPlayer2 org.mpris.MediaPlayer2.Player.Previous