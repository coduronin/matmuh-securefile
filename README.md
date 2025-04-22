# Project Overview

**SecureFile** is a web-based tool designed to secure file uploads by checking for malware. It automatically verifies whether the uploaded document is safe by comparing its hash with known malware hashes from reputable sources such as Malware Bazaar.

When a user uploads a document, SecureFile computes the file's hash and checks it against a predefined list of malware hashes. If a match is found, the file is flagged as potentially malicious. If no match is found, the file is considered safe to upload.

## How it Works

1. **File Upload:** The user uploads a document through the web interface.
2. **Hash Calculation:** The system computes the hash (e.g., SHA256) of the uploaded document.
3. **Hash Comparison:** The calculated hash is compared against a list of known malware hashes fetched from an API (e.g., Malware Bazaar).
4. **Result Action:**
    - **Malware Detected:** If the uploaded file's hash matches any known malware hash, the file is flagged, and security actions are triggered (e.g., alerting the user, rejecting the upload).
    - **Safe to Upload:** If no match is found, the document is allowed to be uploaded and stored securely.
