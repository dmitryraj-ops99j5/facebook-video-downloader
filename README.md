# facebook-video-downloader

A lightweight command line tool to download Facebook videos and reels. It extracts direct MP4 links from standard, watch, and mobile Facebook URLs without external scraper dependencies. Supports private videos via Netscape/JSON cookie files.

## Installation

Clone the repository and install the single dependency:

```cmd
pip install -r requirements.txt
```

## Usage

Pass the video URL as the primary argument. By default, it attempts to download the highest quality available (HD).

```cmd
python fbdown.py "https://www.facebook.com/watch/?v=1234567890"
```

### Options

*   `-o, --output`: Specify the output path or filename. If omitted, it derives a name from the video ID.
*   `-q, --quality`: Force `sd` or `hd` quality (defaults to `hd`).
*   `-c, --cookies`: Path to a Netscape or JSON cookies file for downloading private videos.

```cmd
python fbdown.py "https://www.facebook.com/reel/987654321" -q sd -o my_video.mp4 -c cookies.txt
```

<!-- checked: 2026-09-15 -->
