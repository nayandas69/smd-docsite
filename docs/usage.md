---
title: Usage Guide 🪴
---

Ready to download videos like a pro? This guide will walk you through how to use **Social Media Downloader** in a variety of ways — from Python scripts to native `.exe`, `.deb`, and binary files.

---

## Running the Tool (Python Version)

If you’ve cloned the repo and set up your Python environment, you can launch the tool using:

```bash
python3 downloader.py
```

The tool will start and prompt you for a **public** video URL — just paste the link, and the downloader will handle the rest!

!!! warning
    This tool supports only **public** videos. Private or password-protected content is **not supported**.

---

## Example

```bash
Enter URL: https://www.youtube.com/watch?v=example
```

Once you press Enter, the video will be processed and downloaded automatically.

---

## Using the `.deb` Package

For Debian-based systems (like Ubuntu), we provide a prebuilt `.deb` package so you can install it just like any other app.

### Step-by-step:

1. Download the latest `.deb` file from the [Releases](https://github.com/nayandas69/Social-Media-Downloader/releases/latest) page.
2. Run the following command in your terminal:

```bash
sudo dpkg -i social-media-downloader_VERSION_amd64.deb
sudo apt-get install -f
```

This installs the tool system-wide. Now you can launch it directly with:

```bash
smd
```

That’s it — you’re good to go!

---

## Using the `.exe`

On Windows, we offer a standalone `.exe` file that requires **no setup**.

### How to use:

1. Head to the [latest release](https://github.com/nayandas69/Social-Media-Downloader/releases/latest).
2. Download the `.exe` file.
3. Double-click it. A terminal window will open.
4. Paste your video URL when prompted.

**No Python, no installs — just click and run.**

---

## Using the Linux Binary

For other Linux distributions, you can grab the prebuilt binary file.

### Here’s how:

1. Go to the [Releases page](https://github.com/nayandas69/Social-Media-Downloader/releases/latest) and download the zipped binary.
2. Extract the archive.
3. Navigate to the folder in your terminal and run:

```bash
chmod +x smd
./smd
```

Now you're running the tool natively on Linux!

---

## Installing via pip

You can also install the downloader as a global Python CLI tool using `pip`:

```bash
pip install social-media-downloader
```

Once installed, you can run the tool with:

```bash
social-media-downloader
```

or, on the latest version (`v1.1.4` and up):

```bash
smd
```

---

## CLI Shortcuts: `smd` vs `social-media-downloader`

Starting from version `1.1.4`, we've added a shorthand command to make your life easier:

* `social-media-downloader` → Full command (works in all versions)
* `smd` → Short and sweet (available from `v1.1.4` onward)

!!! note
    Earlier versions (1.0.0 to 1.1.3) **do not** support the `smd` shortcut. If you prefer using the short command, make sure you're on the latest version. That's only for pip.

---

## Pro Tip: Stay Updated

We’re always improving the tool, adding features, and making it even easier to use. Be sure to:

* Check our [Changelog](./changelog.md) for new features
* Follow the [GitHub Releases](https://github.com/nayandas69/Social-Media-Downloader/releases)
* Keep your version up-to-date for the latest improvements

---

Happy downloading!