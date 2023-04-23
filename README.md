<div align="center">

# ytdl-index

*Generates index.html's for your downloaded videos.*

</div>

## Installing

#### Clone repository and install requirements

    git clone ...
    cd ytdl-index
    pip3 install -r requirements.txt


## Example

#### Download video with metadata and thumbnail

    yt-dlp --write-info-json --no-clean-info-json --write-thumbnail https://www.youtube.com/watch?v=PkPSDOjhxwM

#### Generate index.html

    ./run.py .


## Usage

```
usage: run.py [-h] [-s SORT] [-n] [-t TITLE] [-i INFO] [-p PAGE_INFO] [-d DATE_FORMAT] [-a] [-v] [directory ...]

Generate directory listing for files downloaded using youtube-dl / yt-dlp.

positional arguments:
  directory

optional arguments:
  -h, --help            show this help message and exit
  -s SORT, --sort SORT  comma separated list of fields to sort videos by (prefix with + to sort ascending)
  -n, --natsort         sort videos using natsort (useful for titles)
  -t TITLE, --title TITLE
                        page title
  -i INFO, --info INFO  comma separated list of fields to show below video title
  -p PAGE_INFO, --page-info PAGE_INFO
                        comma separated list of fields to show below main title (available: (v)ideos, (s)ize, (d)ate)
  -d DATE_FORMAT, --date-format DATE_FORMAT
                        date format to use
  -a, --show-all
  -v, --verbose

available fields: t = title, u = uploader, v = views, d = date, m = mtime, s = size, l = length, i = index, e = extension
```

## yt-dlp flags

    --write-info-json
    --no-clean-info-json
    --write-thumbnail