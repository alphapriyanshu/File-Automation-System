# 🗂️ Automated File Organizer using Python

![File Automation System](assets/banner.png)

A simple yet powerful Python script that **automatically organizes your downloads folder** by monitoring file changes and moving them into appropriate subfolders (audio, video, images, documents, etc.) using the `watchdog` library.

---

## 📁 Features

- 📦 **Real-time folder monitoring**
- 🎵 Automatically detects and moves audio (music/SFX) files
- 🎬 Sorts video files to a dedicated directory
- 🖼️ Organizes images into an image folder
- 📄 Moves documents like PDFs, Word, Excel, etc.
- 🧠 Intelligent size-based detection for SFX vs Music
- 💥 Handles file name conflicts with unique renaming

---

## 📸 Screenshot Example

> **Before** and **After** organization in the Downloads folder:

| Before | After |
|--------|-------|
| ![Before](assets/before.png) | ![After](assets/after.png) |

---

## 🔧 Tech Stack

- 🐍 Python 3
- 📦 [watchdog](https://pypi.org/project/watchdog/)
- 📂 os, shutil, time, logging

---

## 🧪 How It Works

1. Watches the **Downloads** directory continuously.
2. When a file is added or modified, it checks its type and moves it:
   - `.mp3`, `.wav` → `/music` or `/sfx` (based on size)
   - `.mp4`, `.avi`, etc. → `/video`
   - `.jpg`, `.png`, etc. → `/image`
   - `.pdf`, `.docx`, `.xlsx`, etc. → `/documents`
3. If a file with the same name exists in the destination, a unique name is generated (e.g., `file(1).pdf`).

---

