# File Verifier

A Python tool to verify file types, scan archives (ZIP, RAR, 7z, TAR, GZIP), calculate file hashes, and optionally scan for malware using VirusTotal

## Features
- Verifies file extensions against MIME types using `python-magic`.
- Supports archives: `.zip`, `.rar`, `.7z`, `.tar`, `.gz`, `.tar.gz` with recursive verification.
- Handles password-protected archives.
- Calculates file size, CRC32, and MD5 hashes.
- Optional malware scanning with VirusTotal (cloud-based)
- GUI with drag-and-drop, batch processing, and result saving.
- CLI mode for advanced users.

## Installation
### Prerequisites
- Python 3.6+.
- Install dependencies:
  ```bash
  pip install -r requirements.txt