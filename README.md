
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
To try it please tun this command:

```bash
curl -X POST https://web-terminal-eight.vercel.app/run -H "Content-Type: application/json" -d '{"command": "ls -l"}'
```
Here is a screenshot of the terminal:

![Screenshot 2024-07-27 8 42 42 AM](https://github.com/user-attachments/assets/1b272ece-2215-4777-b84f-1b01e14a18f6)



It uses AWS with a Node.js runtime deployed on Vercel.

This can be proven by typing the `typeset` command in the terminal.
