# EWB Phishing URL Awareness Checker

## Overview
Phishing is a trick in which fake links or messages try to make people reveal private information. This beginner-friendly Python tool reads a URL as text and reports selected warning signs. It never opens the URL or sends it to an online service.

## Features
- Detects an `@` symbol in the URL
- Flags URLs longer than 100 characters
- Flags IP-address hostnames
- Flags hostnames with five or more dot-separated parts
- Flags punycode-style hostnames containing `xn--`
- Flags the HTTP scheme
- Allows repeated checks until the user types `q`, `quit`, or `exit`
- Handles malformed URL text without crashing
- Shows a “Review carefully” summary when warning signs are found

## Requirements
- Python 3.10 or later
- No extra packages are required

## How to Run
Open a terminal in this project folder.

Windows:
```bash
python phishing_checker.py
```

Mac/Linux:
```bash
python3 phishing_checker.py
```

Enter one of the sample URLs from `tests/test_samples.md`. Type `q` to exit.

## Example Output
```text
EWB Phishing URL Awareness Checker
Text checks only - this program does not open URLs.
Use workbook sample URLs only. Type q to quit.

Enter a sample URL (or type q to quit): http://192.0.2.10/account

Result:
- Uses an IP address instead of a familiar domain.
- Uses HTTP. HTTPS alone does not prove trust.

REVIEW CAREFULLY: 2 warning sign(s) found.
Never enter passwords from unexpected links.
```

## Testing
See [`tests/test_samples.md`](tests/test_samples.md) for five sample cases and their expected/actual observations. Run each sample on your computer and verify the results before submitting.

## Screenshots
After running the program locally, save real screenshots with these exact names:
- `screenshots/sample_run.png` — terminal showing the command, sample URL and output
- `screenshots/test_results.png` — the completed test table or evidence of all five test runs

Do not use fabricated screenshots; capture your own computer's output.

## Improvements
1. **Repeat-check loop:** The user can inspect several sample URLs without restarting the program and can type `q` to quit. Tested by entering more than one sample and then quitting.
2. **Malformed input handling and review summary:** Invalid URL formats return a clear message instead of crashing. The program also counts warning messages in a “REVIEW CAREFULLY” summary. Test with the workbook's sample URLs and the malformed sample `http://[bad`.

## Limitations
This is an educational awareness tool. It checks only six visible text clues. It does not visit URLs, scan for malware, check website reputation or prove that a URL is safe. “No listed warning signs found” does NOT mean a URL is safe.

## Ethical Use
Use only the sample strings provided in the workbook. Do not collect credentials, send phishing messages, or test websites without permission. Never put passwords, API keys, or private information in this repository.

## Author
[Replace with your name]  
[Replace with your batch/course]  
EWB Cybersecurity Internship
