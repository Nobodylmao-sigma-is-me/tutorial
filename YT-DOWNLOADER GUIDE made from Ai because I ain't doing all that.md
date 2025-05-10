Termux YouTube Downloader Installation and Usage Guide

Installation (One-Line Script)

Paste the following command into your Termux session:

pkg update -y && pkg install -y python git && pip install --upgrade pip setuptools wheel && pip install requests termcolor beautifulsoup4 && git clone https://github.com/DrDelin/Youtube-Downloader-Android.git && cd Youtube-Downloader-Android && chmod +x install.sh && ./install.sh && mkdir -p ~/bin && curl -Ls https://raw.githubusercontent.com/DrDelin/Youtube-Downloader-Android/master/termux-url-opener | sed '1s|^.*$|#!/data/data/com.termux/files/usr/bin/bash|' > ~/bin/termux-url-opener && chmod +x ~/bin/termux-url-opener

Important Notes

Do not go AFK while this runs. You may be prompted to type Y during package installations.

After installation, you may need to run:

termux-setup-storage

...to allow Termux access to your shared storage.



---

How to Use the Downloader

1. Open YouTube, TikTok, or any supported media app.


2. Tap Share on the video, playlist, or channel.


3. Tap More and select Termux.


4. The downloader interface will pop up with four options:



Menu Options When Sharing a Link

1. Best (Shortcut: b)

Automatically chooses the best quality audio+video.

Ideal for users who just want the highest quality without extra steps.


2. Advanced (Shortcut: m)

Shows a green list of available formats.

Each green line contains an ID, encoding details, and media type.

Type the ID to select a format.

Useful if you want to choose specific quality or encoding.

Caution: Not beginner-friendly due to technical jargon.


Legend:

video only = has video and audio (despite the name)

audio only = audio track only


3. Audio (Shortcut: a)

Lets you choose audio-only download.

After choosing, it asks what format to convert to (e.g., mp3, m4a).

Tip: mp3 offers best compression and cross-platform support.


Works on many platforms, not just YouTube.


4. Video (Shortcut: v)

Lets you choose resolution for video (e.g., 1080p, 720p, 480p, etc.).

Works for single videos, playlists, and full channels.


Subtitle Options (All Modes)

Prompt: "Do you want subtitles?"

Type skip! to skip subtitle download.

Type y to embed subtitles into the video.




---

Where Are Downloads Saved?

Downloads are stored in: ~/storage/shared/Termux_Downloader/

Inside that folder, content is organized by platform:

youtube/

tiktok/

etc/




---

Summary of Shortcut Keys


---

You’re now set to download videos, audio, playlists, and channels directly through Termux with custom options and formats!

