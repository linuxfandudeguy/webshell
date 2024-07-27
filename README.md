
# WebShell
![costume1 (1)](https://github.com/user-attachments/assets/e694a042-cc9e-426b-a6b2-596b2314f7ce)

WebShell is a browser-based Linux terminal experience meant for **development and testing**, and was made as an experiment to see if the node.js module `child_process` with the export `exec` could power an entire terminal, and was also made in need of terminal technologies in the browser.


WebShell is a RHEL based terminal.

The distro that it uses is **Amazon Linux** which is based on **Fedora/CentOS**.

WebShell has a API:
```http
URL: https://web-terminal-eight.vercel.app/run
Method: POST
Headers: Content-Type: application/json
Body: {"command": "your_linux_command_here"}
```
