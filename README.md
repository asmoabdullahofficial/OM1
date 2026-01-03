## Beginner Troubleshooting Tips (For WSL on Windows Users)

If you're a non-technical beginner setting up OM1 on Ubuntu via WSL (Windows Subsystem for Linux), here are some common issues and fixes based on real experience:

### 1. Network Unreachable Error During `sudo apt update`
- Issue: Commands like `sudo apt update` fail with "Network is unreachable".
- Fix: Restart WSL in PowerShell (run as admin): `wsl --shutdown`. Then reopen Ubuntu and retry.

### 2. Build Errors During `uv sync`
- Issue: Errors like "command 'cc' failed" or "portaudio.h: No such file or directory".
- Fix: Install missing packages: `sudo apt install build-essential python3-dev portaudio19-dev -y`.

### 3. Config Syntax Errors in spot.json5
- Issue: Editing api_key leads to "Unexpected '"' or similar syntax errors due to quotes/commas.
- Fix: Use unquoted keys and always add comma at end, e.g.: `api_key: "your_key_here",`. Use nano editor and double-check.

### 4. No Interaction Options in WebSim UI<a href="http://localhost:8000/" target="_blank" rel="noopener noreferrer nofollow"></a>
- Issue: UI shows state (e.g., actions/emotions) but no text box or mic button for commands.
- Fix: Ensure mic/webcam permissions in Windows. Suggestion: Add text input in UI for fallback.

### 5. Credits Not Deducted and Blockchain 503 Error
- Issue: Portal shows $0 used; terminal logs "Loading rules from Ethereum blockchain failed with 503".
- Fix: Interact via voice/commands to trigger API calls. 503 is temporary server issue – retry after 10-15 mins.

These tips would make setup easier for beginners. Thanks!