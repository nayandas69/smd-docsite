---
title: Installation
---

Let’s get you up and running with **Social Media Downloader** — a powerful command-line tool to grab public videos from platforms like YouTube, TikTok, and more.

Follow the steps below to set up the project locally on your system.

---

## Clone the Repository

Start by cloning the official GitHub repository to your local machine:

```bash
git clone https://github.com/nayandas69/Social-Media-Downloader.git
cd Social-Media-Downloader
```

---

### Set Up the Python Environment

!!! tip
    We recommend using **Python 3.8+** and setting up a virtual environment to keep things clean and organized.

### On Windows

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python smd/downloader.py
```

### On Linux

```bash
python3 -m venv venv
source venv/bin/activate
pip3 install -r requirements.txt
python3 smd/downloader.py
```

---

# Install ffmpeg (Required)

!!! important
    The downloader relies on **ffmpeg** to process video and audio. Make sure it's installed and added to your system’s PATH.

Here’s how to install it:

## On Windows

* Download from: [https://ffmpeg.org/download.html](https://ffmpeg.org/download.html)
* Extract the ZIP
* Add the `bin` folder to your `PATH` environment variable

## On Linux

```bash
sudo apt update
sudo apt install ffmpeg
```

To confirm installation:

```bash
ffmpeg -version
```

If you see the version info, you’re good to go!

---

## You’re Ready!

Now you can start downloading:

```bash
python3 smd/downloader.py
```

That’s it — you’ve set up the Social Media Downloader!

!!! tip
    Want to use the Build Artifacts `.exe`, `.tar.gz`, or `.deb` instead of building manually? Visit the [Release Archive](./archive.md).


---

## See Also
* [Usage Instructions](./usage.md) - Learn how to use the downloader effectively.
* [Build Instructions](./build.md) - Customize your build with icons, silent mode, and more.
* [Troubleshooting](./troubleshooting.md) - Common issues and how to fix them.
* [Release Archive](./archive.md) - Build Artifacts binaries for easy installation.
* [Contributing](./contribute.md) - Join the community and help improve the project.
* [FAQ](./faq.md) - Frequently asked questions and answers.