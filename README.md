# OnlineClassWatcher

The **OnlineClassHelper** automates the process of attending online classes by interacting with the UOOC platform. This includes retrieving the list of unfinished courses, selecting a course, and automating video watching for a smooth learning experience. The script utilizes **ffmpeg** to handle video playback and tracks the progress of video lectures.

---

## Features

### 1. Course List Retrieval
The script fetches the list of ongoing courses from the UOOC platform and allows the user to select a course by its index.

### 2. Catalog Parsing
After selecting the course, the system fetches the course catalog, identifies available lessons, and lists the sections and videos that need to be watched.

### 3. Video Downloading and Playback
The script uses **ffmpeg** to download videos, determine their lengths, and control video playback. It then updates the progress of the videos being watched.

### 4. Learning Progress Update
As videos are watched, their progress is uploaded to the platform to track attendance, ensuring the system is marked as completed on the UOOC platform.

---

## Technology Stack
- **Language**: Python
- **Libraries**: requests, json, time, os, subprocess
- **Video Processing**: ffmpeg
- **Platform**: UOOC (优课平台)

---

## Workflow & Process

### 1. Get Courses
The first step is retrieving the list of courses and selecting the course the user wants to attend.

### 2. Get Catalog
The course catalog is fetched, identifying all the available chapters, sections, and subsections. The system then identifies which videos need to be watched.

### 3. Get Unit Video IDs
For each chapter and section, the script extracts the video IDs, ensuring that only unfinished videos are processed.

### 4. Mark Video Progress
After the videos are downloaded and played, the system continuously uploads the watch progress to the platform, ensuring that the video’s watch status is updated.

---

## Setup Instructions

### 1. Configure `ffmpeg` Path
Ensure that the **ffmpeg** binary is installed on your system. You need to specify the **path to the ffmpeg binary** in the script. Example:
```python
ffmpeg_path = os.path.join('D:/ffmpeg/ffmpeg', 'bin', "ffprobe.exe")
