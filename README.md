# PoC artifacts

Supporting artifacts for the security advisory in this repository.

## microsoft_playwright_mcp_0.0.47_file_exfil.mp4

[▶ View video](https://github.com/mmzha2013/security-research/raw/main/PoC/microsoft_playwright_mcp_0.0.47_file_exfil.mp4)

Demonstrates `/etc/passwd` exfiltration against `@playwright/mcp@0.0.47`
from https://github.com/microsoft/playwright-mcp, running via the official
Docker image `mcr.microsoft.com/playwright/mcp`. The recording begins at
the MCP-host prompt stage; the preceding Docker image pull and MCP client
configuration follow the upstream documented procedure.

## cloudflare_playwright_mcp_0.0.5_file_exfil.mp4

[▶ View video](https://github.com/mmzha2013/security-research/raw/main/PoC/cloudflare_playwright_mcp_0.0.5_file_exfil.mp4)

Demonstrates the same exfiltration primitive against `cloudflare/playwright-mcp`
v0.0.5 from https://github.com/cloudflare/playwright-mcp. The recording
begins at the MCP-host prompt stage; the preceding repository clone and
build steps follow the upstream documented procedure and are identical to
those in the upstream variant above.

## upload_server.py

[📄 View code](https://github.com/mmzha2013/security-research/blob/main/PoC/upload_server.py)

Attacker-side Flask receiver used in both videos.

## Note on `/etc/passwd`

`/etc/passwd` is a world-readable Linux system file used here as the
standard benign demonstration target for this class of vulnerability.
It contains no credentials; password hashes reside in `/etc/shadow`
(root-only access). No sensitive data is disclosed by the demonstrations.
