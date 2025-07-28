# File Verifier

A Python tool to verify file types, scan archives (ZIP, RAR, 7z, TAR, GZIP), calculate file hashes, and optionally scan for malware using VirusTotal.

## Features

- Verifies file extensions against actual file types using magic numbers.
- Supports archive formats: `.zip`, `.rar`, `.7z`, `.tar`, `.gz`, `.tar.gz` with recursive scanning.
- Detects and handles password-protected archives.
- Calculates file size, CRC32, and MD5 hashes.
- Optional malware scanning using VirusTotal (cloud-based).
- GUI with drag-and-drop support, batch processing, and result saving.
- CLI mode for advanced users and scripting.

## Installation

### Prerequisites

- Python 3.6 or higher

Install dependencies:

```bash
pip install -r requirements.txt
````

### For `.rar` support:

* **Windows**:
  Download `UnRARDLL.exe` from [rarlab.com](https://www.rarlab.com/rar/UnRARDLL.exe) and place `unrar.dll` in `C:\Windows\System32` or your project directory.

* **Linux (Debian/Ubuntu)**:

  ```bash
  sudo apt install unrar
  ```

* **Fedora**:

  ```bash
  sudo dnf install unrar
  ```

* **macOS**:

  ```bash
  brew install unrar
  ```

### For VirusTotal:

* Sign up and get a free API key from [VirusTotal](https://www.virustotal.com/gui/join-us).

## Setup

Clone the repository:

```bash
git clone https://github.com/your-username/file-verifier.git
cd file-verifier
```

Install Python dependencies:

```bash
pip install -r requirements.txt
```

Run the program:

```bash
python file_verifier.py
```

## Usage

### GUI Mode

Launch the graphical interface:

```bash
python file_verifier.py
```

* Drag and drop files or folders.
* Enter your VirusTotal API key if malware scanning is desired.
* View and save verification results.

### CLI Mode

Run from the command line:

```bash
python file_verifier.py /path/to/file
```

Example output:

```
=== Verifying sample.mp3 ===
✅ OK: Extension '.mp3' matches its type (audio/mpeg)
📏 Size: 3,816,027 bytes
🔗 CRC32: ef2158cf
🔗 MD5: a0a44fe2ae9a5019bc3a3577ce5db666
✅ VirusTotal: No threats detected
```

## Notes

* **Privacy Warning**: Files sent to VirusTotal are publicly shared — don’t upload sensitive content.
* **Rate Limits**: VirusTotal free API has limits — 4 requests/minute, 500/day.
* **Security Tip**: Always verify files before executing or sharing.

## Support

If this tool helps you verify and secure files, feel free to contribute, report bugs, or suggest features via GitHub issues or pull requests.

