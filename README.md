# PoC artifacts

## microsoft_playwright_mcp_0.0.47_file_exfil.mp4
Demonstrates `/etc/passwd` exfiltration against `@playwright/mcp@0.0.47`
from https://github.com/microsoft/playwright-mcp, running via the official
Docker image `mcr.microsoft.com/playwright/mcp`. User identifiers have been
redacted from the recording. The target file `/etc/passwd` is a world-readable
system file containing no credentials (password hashes live in `/etc/shadow`);
it is used here as the standard benign demonstration target for this class
of vulnerability.

## cloudflare_playwright_mcp_0.0.5_file_exfil.mp4
Demonstrates the same exfiltration primitive against `cloudflare/playwright-mcp`
v0.0.5 from https://github.com/cloudflare/playwright-mcp. The recording begins
at the MCP-host prompt stage; the preceding repository clone and build steps
follow the upstream documented procedure and are identical to those in the
Microsoft variant above.

## upload_server.py
Attacker-side Flask receiver used in both videos.
