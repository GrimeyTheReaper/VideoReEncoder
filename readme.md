# MP4 Reencoder Script
*(WITH .AVI AND .MKV SUPPORT)*

This script helps you re-encode MP4* videos. It monitors a folder for new MP4 files, processes them, and saves the re-encoded versions to a different folder.

It's like having a magical robot that waits for your videos, makes them better (or changes how they look), and then stores them in a special folder for you. Cool, right?

## DEV NOTE: THIS SHOULD WORK ON ALL BROWSERS, I MYSELF HAVE ONLY TESTED IT WITH FIREFOX & CHROME! PLEASE LET ME KNOW [HERE](https://github.com/GrimeyTheReaper/VideoReEncoder/issues) IF THERE ARE ANY PROBLEMS WITH YOUR PARTICULAR BROWSER OF CHOICE!

## How to Use the Script

### 1. Install Python

If you don't have Python installed on your computer, you need it. You can get it from [here](https://www.python.org/downloads/).

### 2. Install Required Libraries

The script relies on some helper tools (called libraries) to run. It will check if they are installed when you run it, and if not, it will notify you which ones are missing.

To install them, open your command prompt (or terminal) and run:

```bash
pip install psutil watchdog colorama
```

If you're unsure what `pip` is, don't worry! The script will guide you if you don't have it installed.

### 3\. Modify the `.json` File for Paths (Windows-specific)

In some cases, especially for Windows users, you may need to adjust the paths in the script's configuration file (a `.json` file). This is because Windows uses backslashes (`\`) in file paths, but Python treats backslashes as escape characters.

**How to modify the `.json` file**:

-   Open the `.json` file used by the script.
-   Locate any file paths (like `INPUT_FOLDER` and `OUTPUT_FOLDER`).
-   Ensure that each backslash is doubled. For example:
    -   Original: `C:\Users\YourName\Videos\Downloads`
    -   Modified: `C:\\Users\\YourName\\Videos\\Downloads`

This modification ensures the script correctly interprets the file paths.

### 4\. Prepare the Folders

-   Place the script (`VideoReEncoder.py`) AND the cfg file (`config.json`) in any folder you like.
-   Create a folder where your MP4* (downloaded files) will go, called `INPUT_FOLDER`, and add some MP4* videos to it.
-   Create another folder where the re-encoded videos will be saved, called `OUTPUT_FOLDER`.

For example:

-   `INPUT_FOLDER`: `C:\\Users\\YourName\\Videos\\Downloads`
-   `OUTPUT_FOLDER`: `C:\\Users\\YourName\\Videos\\Reencoded`

### 5\. Run the Script

-   Open your command prompt (or terminal).
-   Navigate to the folder where the script is stored.
-   Run the script by typing:

`python VideoReEncoder.py `

Alternatively, you can **double-click** the script to run it.

The script will start monitoring the input folder, and when a new MP4* file is added, it will start processing it.

### 6\. Enjoy!

After the script finishes processing, it will save the re-encoded video to the output folder. 🎉

* * * * *

License and Credits
-------------------

This script uses the following:

1.  **FFmpeg**: FFmpeg is a free software that helps convert and encode video and audio files.

    -   License: FFmpeg is licensed under the GNU General Public License (GPL) version 2 or later.
    -   You can download FFmpeg [here](https://www.ffmpeg.org/download.html).
    -   More information on FFmpeg's license can be found [here](https://www.ffmpeg.org/legal.html).
2.  **psutil Library**: This library helps the script check if certain programs are already running on your computer.

    -   License: MIT License (free to use, modify, and share).
    -   You can download psutil [here](https://pypi.org/project/psutil/).
3.  **watchdog Library**: This library enables the script to "watch" a folder for new files.

    -   License: MIT License (free to use, modify, and share).
    -   You can download watchdog [here](https://pypi.org/project/watchdog/).
4.  **colorama Library**: This library adds colors to the text in your command prompt, making the script more visually appealing.

    -   License: MIT License (free to use, modify, and share).
    -   You can download colorama [here](https://pypi.org/project/colorama/).

* * * * *

What if Something Goes Wrong?
-----------------------------

1.  **Error Messages**: If something goes wrong, the script will display an error message such as "Error: Library 'psutil' is missing. Please install it using pip."

2.  **Don't Panic**: If you encounter an error, read the message carefully. It will usually tell you exactly what to do to fix the problem. Most errors happen because a required library is missing, and the script will guide you through fixing it.

* * * * *

Special Thanks
--------------

A huge thank you to the developers of FFmpeg, psutil, watchdog, and colorama. These amazing tools made it easy for me to build this script!
This modification ensures the script correctly interprets the file paths.


## Troubleshooting

### **Missing Libraries**
If the script reports that a library is missing (e.g., "Error: Library 'psutil' is missing"), simply follow the suggestion and install it using pip:

`pip install <library-name>`


### **FFmpeg Not Installed**
The script will notify you if FFmpeg is not installed on your system. You can download FFmpeg from the official site: [FFmpeg Download](https://www.ffmpeg.org/download.html).

### **File Not Ready for Processing**
If the script detects a new video file but is unable to process it, it might be because the file is still being downloaded or written to. The script will wait until the file is ready, but if it doesn’t stabilize, it will skip the file.


## GitHub Repository

You can find the source code and contribute to the project on GitHub. Feel free to explore and provide any feedback or improvements!

**Repository**: [GrimeyTheReaper/VideoReEncoder](https://github.com/GrimeyTheReaper/VideoReEncoder)

---

Thanks for using the MP4 Reencoder Script! 🎬
