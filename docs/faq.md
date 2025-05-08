---
title: ❓ Frequently Asked Questions
---

Welcome to the FAQ section for **Social Media Downloader**! Here, we've compiled answers to the most common questions to help you get the most out of our tool.

---

### 1. What is Social Media Downloader?

**Social Media Downloader** is a command-line tool designed to download public videos, reels, and posts from platforms like YouTube, TikTok, Instagram, Facebook, and more. It's lightweight, open-source, and supports batch downloads, making it a versatile choice for users across different operating systems.

---

### 2. Which platforms are supported?

Currently, the tool supports downloading content from:

- **YouTube**
- **TikTok**
- **Instagram**
- **Facebook**   

and See the [Supported Platforms](./supported-platforms.md) page for more details.
We're continually working to expand support to more platforms in future updates.

---

### 3. Is the tool free to use?

Absolutely! Social Media Downloader is open-source and completely free. You can view, modify, and distribute the code under the terms of the [MIT License](https://github.com/nayandas69/Social-Media-Downloader/blob/main/LICENSE).

---

### 4. Does it support downloading private or password-protected content?

No. The tool is designed to download **public** content only. It does not support downloading private or password-protected videos, ensuring compliance with platform policies and user privacy.

---

### 5. How do I install the tool?

You can install Social Media Downloader using pip:

```bash
pip install social-media-downloader
```

Alternatively, you can clone the repository:

```bash
git clone https://github.com/nayandas69/Social-Media-Downloader.git
cd Social-Media-Downloader
```

For detailed installation instructions, refer to the [Installation Guide](./installation.md).

---

### 6. How do I use the tool after installation?

After installation, you can run the tool using:

```bash
social-media-downloader
```

Or, if you have version 1.1.4 or later:

```bash
smd
```

Follow the on-screen prompts to enter the URL of the content you wish to download.

---

### 7. What file formats are supported for downloads?

The tool supports downloading videos in various formats, including MP4 and MP3. You can choose the desired format during the download process.

---

### 8. Can I download multiple videos at once?

Yes! Social Media Downloader supports batch downloads, especially for platforms like Instagram. You can input multiple URLs, and the tool will process them sequentially.

!!! warning
    Only support Instagram

---

### 9. Is there a graphical user interface (GUI) available?

Currently, Social Media Downloader is a command-line tool and does not have a GUI. However, we're exploring the possibility of developing a GUI in future releases.

---

### 10. How do I update the tool to the latest version?

If you installed the tool using pip, you can update it using:

```bash
pip install --upgrade social-media-downloader
```

For other installation methods, refer to the [Installation Guide](./installation.md) for update instructions.

---

### 11. I'm encountering a "ModuleNotFoundError" related to pyfiglet fonts. How can I fix this?

This error occurs when PyInstaller misses the font files during the build process. To fix it:

1. Create a spec file:

   ```bash
   pyi-makespec --onefile downloader.py
   ```

2. Edit the generated `downloader.spec` file and add:

   ```python
   from PyInstaller.utils.hooks import collect_data_files
   datas = collect_data_files("pyfiglet")
   ```

3. Rebuild the executable:

   ```bash
   pyinstaller downloader.spec
   ```

For more details, refer to the [Troubleshooting Guide](./troubleshooting.md).

---

### 12. Does the tool work on both Windows and Linux?

Yes! Social Media Downloader is cross-platform and works seamlessly on both Windows and Linux systems. We provide `.exe` files for Windows and binaries or `.deb` packages for Linux.

---

### 13. Is there a way to contribute to the project?

Absolutely! We welcome contributions from the community. You can fork the repository, make your changes, and submit a pull request. For more details, check out the [Contribute Guide](./contribute.md).

---

### 14. How can I report bugs or request new features?

You can report issues or request features by opening an issue on our [GitHub Issues Page](https://github.com/nayandas69/Social-Media-Downloader/issues). Please provide detailed information to help us address your concerns effectively.

---

### 15. Is there a changelog available to track updates?

Yes, we maintain a [Changelog](./changelog.md) that lists all the updates, improvements, and bug fixes in each version.

---

### 16. Are there any legal considerations I should be aware of?

Yes. Social Media Downloader is intended for downloading **public** content for personal use. Downloading copyrighted material without permission may violate laws in your jurisdiction. Always ensure you have the right to download and use the content.

---

### 17. Can I use the tool without installing Python?

Yes! For users who prefer not to install Python, we provide standalone executables (`.exe` for Windows and binaries for Linux) that can be run directly. Check out the [Releases Page](https://github.com/nayandas69/Social-Media-Downloader/releases) for the latest versions.

---

### 18. How do I uninstall the tool?

If you installed the tool using pip, you can uninstall it using:

```bash
pip uninstall social-media-downloader
```

For other installation methods, refer to the [Installation Guide](./installation.md) for uninstallation instructions.

---

### 19. Does the tool support downloading stories or live videos?

Currently, Social Media Downloader focuses on downloading standard posts and videos. Support for stories and live videos is not available at this time.

---

### 20. Where is the downloaded content saved?

By default, all videos and audio files are saved in a folder named `media`, which is automatically created in the current directory when you run the CLI. You can change this folder by editing the `"download_directory"` value in the `config.json`.

---

### 21. What is `config.json` and what does it do?

The `config.json` file is automatically created the first time you run Social Media Downloader. It stores key settings like:

```json
{
  "default_format": "show_all",
  "download_directory": "media",
  "history_file": "download_history.csv",
  "mp3_quality": "192"
}
```

Here’s what each field means:

* **default\_format**: Controls the default download behavior (e.g., show all formats or auto-select best).
* **download\_directory**: The folder where all your media gets saved. It's automatically created if it doesn't exist.
* **history\_file**: Keeps a log of everything you've downloaded in `.csv` format — useful for tracking and avoiding duplicates.
* **mp3\_quality**: Controls the bitrate of MP3 audio (default is 192 kbps). You can increase this to `"256"` or `"320"` for higher audio quality.

!!! danger
    When you run the tool from a new or different path, it will automatically create a fresh `config.json`, `media` folder, and `download_history.csv`.  
    If you're just starting out, we recommend running it from your **Desktop** so everything stays organized.  
    You can always open `config.json` and customize settings like `download_directory`, `default_format`, or `mp3_quality` later on.

The best part? This app doesn’t send or track any of your data — everything is stored locally, and you're always in control.

---

### 22. What is `config.json` and where can I find it?

`config.json` is an auto-generated configuration file that appears when you first run the tool. It contains default settings like download location, MP3 quality, and history tracking. It lives in the same folder as your `downloader.py` or executable.

---

### 23. Can I change the default MP3 quality?

Yes! Open `config.json` and modify the `"mp3_quality"` field. The default is `"192"`, but you can set it to a higher bitrate like `"256"` or `"320"` for better audio fidelity.

```json
"mp3_quality": "320"
```

Make sure you have `ffmpeg` installed, as it handles the audio conversion.

---

### 24. What does `download_history.csv` do?

This file keeps track of everything you’ve downloaded using the CLI — including URLs, timestamps, and formats. It helps avoid downloading the same link twice and gives you an audit trail for your activity.

---

### 25. What’s inside `downloader.log`?

That’s the logging file! If the tool crashes or something doesn’t work, check `downloader.log`. It captures error messages, failed downloads, and other useful debug information that can help you or developers fix bugs.

---

### 26. Does this tool collect or track any personal data?

**No.** Social Media Downloader is 100% local. It doesn't send your URLs, history, or any information to a server. There’s no backend, no analytics, no tracking — everything is stored on your own machine.

---

### 27. Can I use this tool offline?

Yes, partially. Once the dependencies are installed and `ffmpeg` is available locally, you can use the tool to download videos as long as you have internet access for the video sources. The tool itself doesn’t require an active connection to operate internally.

---

### 28. What libraries does this tool use?

The tool is built with powerful, open-source libraries:

* `yt-dlp`: handles video downloads
* `instaloader`: supports Instagram content
* `tqdm`: for beautiful progress bars
* `requests`: for HTTP calls
* `ffmpeg-python`: for media conversion
* `tabulate`, `termcolor`, `pyfiglet`: for better CLI experience

For the full list, check `requirements.txt`.

---

### 29. I’m concerned about dependencies. Is it safe?

Yes, the dependencies used are from reputable sources and open-source communities. You can audit the code and even build the tool yourself from source if you’re extra cautious.

---

### 30. How do I build my own `.exe` or `binary` from source?

You can follow our [Build Instructions](./build.md) to package the tool into a standalone executable or binary for your system. We use GitHub Actions to generate releases, but you're encouraged to build locally if you prefer.

---

### 31. Why should I trust this project?

* Open-source under MIT License
* No tracking, telemetry, or backend
* All data is saved **locally**
* You can inspect or modify the code freely
* All binaries are auto-built with GitHub Actions — no hidden installers

---

### 32. I want to contribute, but I don’t know where to start?

Check our [Contributing Guide](./contribute.md) for simple steps to begin. You don’t need to be an expert — even fixing typos or improving documentation helps a lot!

---

### 33. Can I use a `.txt` file with multiple links?

Absolutely! Just create a `.txt` file with one URL per line, and the CLI will read it and download each link sequentially. This works for Instagram supported .

---

### 34. How does the tool handle updates?

The tool includes a built-in update **checker** — not an auto-updater. When you run the CLI, it checks if a newer version is available by querying the GitHub Releases API. If an update exists, you'll see a message with the latest version and a link to download it.

However, **you still need to update it manually**. You can:

* Pull the latest code from the GitHub repo if you're running from source:

  ```bash
  git pull origin main
  ```
 Or, if installed via pip, update with:

  ```bash
  pip install social-media-downloader --upgrade
  ```
* If you're using the **.exe**, **binary**, or **.deb** versions of the tool,  
    make sure to manually download the latest release from the [Releases page](https://github.com/nayandas69/Social-Media-Downloader/releases).
    
!!! note
    The update check only runs if you're connected to the internet.  
    It won't download or install anything automatically.  

---

### 35. Can I use this in a Docker container?

Currently, it’s not officially Dockerized — but you're welcome to create your own Docker setup using the Python environment. Just be sure to include `ffmpeg`.

---

### 36. Does it work on ARM-based systems (e.g. Raspberry Pi)?

Yes, as long as Python and `ffmpeg` are available for your architecture, you should be able to run the tool. Use the Python script version, not a prebuilt binary.

---

### 37. Can I change the output filename format?

Not directly right now. However, feel free to modify the naming logic in the Python source if you want to customize filenames based on date, title, or platform.

---

### 38. Is it safe to run as root/admin?

There's no need to run the tool with elevated privileges. It works perfectly in normal user mode. Only use `sudo` if installing system-wide dependencies like `ffmpeg`.

---

### 39. Can I download entire playlists or user channels?

Not yet — currently, the tool supports single video URLs or batch links via `.txt`. Playlist and channel support may come in future versions.

---

### 40. How do I get support?

* For bugs: open an [Issue](https://github.com/nayandas69/Social-Media-Downloader/issues)
* For questions: visit the [Discussions](https://github.com/nayandas69/Social-Media-Downloader/discussions)
* For general help: check the [Troubleshooting Guide](./troubleshooting.md)

---

Need more help? Don’t hesitate to reach out — the community’s here to support you.
We hope this FAQ section helps you navigate and utilize Social Media Downloader effectively. Happy downloading!