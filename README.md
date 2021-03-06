# FORKED FROM XRTce/snapchat-takeout

# snapchat-takeout
## Snapchat Takeout (GDPR) Memories Downloader
### This Python3 application downloads your media files (known as memories) from Snapchat servers to your local disk.

When [requesting your data from Snapchat](https://accounts.snapchat.com/accounts/downloadmydata) they sadly only include a `.json` file which contains a seperate download link for each memory file.
This application parses the `.json` file, then does it's best to download the files to local disk.



### Features:
- File Handling
  - Apply naming sheme (Default: `Snapchat-YYYY-MM-DD_HHMMSS[1..n].ext`)
  - Recursive naming of files created with same timestamp (the optional `[1..n]` part above)
  - Existing Files are skipped
- Error Handling
  - Log failed Downloads
- Restart download at any time (download progress is logged)
- Stats after completion
- Status output while downloading
- Maybe i forgot some, it's been a long day ¯\\\_(ツ)\_/¯

### Disclaimer:

### Usage
1. Put your `memories_history.json` file into the project's root folder
2. Run `app.py`

You should end up with the following file structure:
- `./media/Snapchat-xxx` <-- Your downloaded files
- `./errors.txt` <-- Failed files including failed download links
- `./downloaded.txt` <-- All successfull downloaded Links

If the app is stopped during runtime it resumes after the last downloaded file (for this to work dont delete `downloaded.txt`)
It is possible to change the timezone for appling the file naming sheme, media folder and the file naming sheme inside the code as you should've noticed becuase you read and understood the code ;) 

### Screenshots
Downloading files:
---
![downloading](https://github.com/cmd-k/snapchat-takeout/raw/master/screenshots/downloading.png)

Skipping existing files:
---
![skipped](https://github.com/cmd-k/snapchat-takeout/raw/master/screenshots/skipped.png)

Duplicate file handling:
---
![duplicate](https://github.com/cmd-k/snapchat-takeout/raw/master/screenshots/duplicate.png)

Download error:
---
![error](https://github.com/cmd-k/snapchat-takeout/raw/master/screenshots/error.png)

Stats after finished task:
---
![stats](https://github.com/cmd-k/snapchat-takeout/raw/master/screenshots/stats.png)
