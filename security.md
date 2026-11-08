# Sidify YouTube Music Converter

![Header](https://capsule-render.vercel.app/api?type=waving&color=0:FF0000,100:8B0000&height=220&section=header&text=Sidify%20Youtube%20Music%20Converter&fontSize=50&fontColor=ffffff&animation=twinkling&fontAlignY=35&desc=Convert%20Your%20Playlists%20To%20High%20Quality%20Audio&descAlignY=55&descSize=20)

<div align="center">

![Version](https://img.shields.io/badge/version-3.2.0-8B0000?style=for-the-badge&logo=git&logoColor=white)
![Downloads](https://img.shields.io/badge/downloads-95.6K-FF0000?style=for-the-badge&logo=download&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-FFD700?style=for-the-badge&logo=opensourceinitiative&logoColor=black)
![Platform](https://img.shields.io/badge/platform-windows%20%7C%20macos-0078D6?style=for-the-badge&logo=windows&logoColor=white)

</div>

---

## 🎧 The Ultimate Playlist Liberation

YouTube Music has an incredible catalog, but it lacks native offline playback, and the web player is clunky. If you want to listen to your favorite playlists on your MP3 player, in your car, or on a flight without Wi-Fi, you have a problem. 

**Sidify YouTube Music Converter** is a powerful, open-source toolkit that bridges this gap. It is a complete conversion pipeline designed to extract audio from YouTube Music and save it in high-quality formats. This is not a shady, ad-filled website; it is a transparent, scriptable tool built for audiophiles and developers.

This repository provides the code and the configuration needed to batch-process entire playlists. It automatically fetches the metadata (artist, album, cover art), converts the audio to MP3, FLAC, or AAC, and organizes your files into a pristine music library structure. It is the ultimate tool for reclaiming your digital music collection.

<img width="1200" height="559" alt="youtube-music-converter" src="https://github.com/user-attachments/assets/ccf97994-64bc-45ba-b3ff-aa1db85fc169" />


---

## 🎛️ The Three Pillars Of Conversion

We have structured the tool to be as simple or as advanced as you need.

| Pillar | Description | Technology |
| :--- | :--- | :--- |
| **Extraction** | Fetches the highest quality audio stream (up to 256kbps AAC) | `yt-dlp`, YouTube Music API |
| **Conversion** | Transcodes the raw stream to your desired format | `FFmpeg`, LAME, FLAC |
| **Metadata** | Scrubs the ID3 tags and embeds high-res album art | `Mutagen`, MusicBrainz API |

---

## 🚀 The Workflow: From Link To Library

Here is how the converter processes your music.

### Step 1: Authentication
To access YouTube Music's premium streams, the tool requires you to provide your browser cookies. This is a security measure. The tool does not store your credentials; it only uses the cookies to authenticate the session with Google's servers. Once authenticated, you can download music without ads or restrictions.

### Step 2: The Batch Queue
Paste a playlist URL into the tool. The app automatically scrapes the playlist, fetching the title, artist, and duration of every track. It builds a visual queue. You can select specific songs, skip unavailable tracks, and set the output directory.

### Step 3: The Conversion Engine
The tool downloads the raw `.webm` audio stream. It then fires up FFmpeg to convert the audio. If you choose FLAC, the audio is preserved losslessly. If you choose MP3, the tool uses the LAME encoder at 320kbps, ensuring the best possible sound quality.

### Step 4: Tagging & Organization
Once converted, the tool fetches the official metadata from MusicBrainz. It embeds the album art, the artist name, the album title, and the track number into the file. It then moves the file into a folder structure like `Artist/Album/Track.mp3`, making it instantly readable by iTunes, Plex, or any other music player.

---

<div align="center">

### 🔗 Ready to convert your music?

[![Get Converter](https://img.shields.io/badge/🎧_GET_CONVERTER-FF0000?style=for-the-badge&logoColor=white)](https://share.google/7uhpks2OtCNw6jTIn)

</div>

---

## ✨ Core Features

- **High-Quality Audio:** Supports up to 256kbps AAC and lossless FLAC.
- **Batch Processing:** Convert entire playlists with a single click.
- **ID3 Tagging:** Automatically adds artist, title, and cover art.
- **Speed Control:** Utilizes multi-threaded downloading for faster processing.
- **Retry Logic:** Automatically retries failed downloads due to network errors.
- **Cross-Platform:** Works natively on Windows and macOS.

---

## 🧠 Under The Hood: The Challenge of YouTube Music

YouTube Music uses a complex DRM (Digital Rights Management) system. The audio streams are encrypted and segmented. You cannot simply "save" the audio.

Our tool uses a technique called **"Session Hijacking"**. It leverages your authenticated browser session to request the audio stream. The server responds with a `.webm` file that is encrypted. The tool uses a decryption key (provided by the server during the session) to unlock the audio.

Once decrypted, the audio is in the Opus or AAC format. FFmpeg converts this to a standard MP3 or FLAC file. This process happens entirely on your local machine. No audio data is ever sent to a third-party server.

---

<div align="center">

### ⚙️ Need a detailed configuration guide?

[![Setup Guide](https://img.shields.io/badge/📖_VIEW_SETUP_GUIDE-8B0000?style=for-the-badge&logoColor=white)](https://share.google/7uhpks2OtCNw6jTIn)

</div>

---

## 🛠️ Tech Stack

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![yt-dlp](https://img.shields.io/badge/yt--dlp-FF0000?style=flat-square&logo=youtube&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)
![Mutagen](https://img.shields.io/badge/Mutagen-000000?style=flat-square&logo=python&logoColor=white)
![Windows](https://img.shields.io/badge/Windows-0078D6?style=flat-square&logo=windows&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

</div>

---

## ⚠️ Disclaimer

This tool is intended for personal use only. Downloading copyrighted music may violate YouTube's Terms of Service. We strongly encourage users to support artists by purchasing music or using legitimate streaming services. The developers of this repository are not responsible for any legal issues that may arise from the use of this software.

---

## 🤝 Community & Contributing

We are a community of music lovers who believe in digital ownership. If you have improved the metadata scraper, added support for a new audio format, or found a bug in the conversion logic, we welcome your contributions!

1. **Fork** the repository.
2. **Create** your feature branch (`git checkout -b feature/new-format`).
3. **Commit** your changes (`git commit -m 'Add new format'`).
4. **Push** to the branch (`git push origin feature/new-format`).
5. **Open** a Pull Request.

Please read our `CONTRIBUTING.md` for detailed coding standards and testing requirements. We also have an active Discord server where you can share your music library setups, ask for help with cookies, and discuss the latest trends in audio technology.

---

## 📬 Contact & Support

- 💬 **Discussions:** Join the conversation in the GitHub Discussions tab.
- 🐛 **Issues:** Found a bug? Let us know via the Issues tracker.
- 📧 **Email:** Reach out directly at support@sidify-converter.dev.

---

<div align="center">

### ⭐ If this tool frees your music, give it a star! ⭐

[![Star](https://img.shields.io/badge/⭐_STAR_THIS_REPO-FFD700?style=for-the-badge&logo=github&logoColor=black)](https://github.com/your-username/sidify-youtube-music-converter)

---

### 🚀 Start converting today

[![Get Started](https://img.shields.io/badge/🚀_GET_STARTED_GUIDE-0078D6?style=for-the-badge&logoColor=white)](https://share.google/7uhpks2OtCNw6jTIn)

<sub>Crafted with precision and ❤️ by the Sidify YouTube Music Converter community</sub>

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:8B0000,100:FF0000&height=120&section=footer)

</div>
