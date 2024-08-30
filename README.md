

# WebShell

![costume1 (1)](https://github.com/user-attachments/assets/e694a042-cc9e-426b-a6b2-596b2314f7ce)

WebShell is a browser-based Linux terminal experience designed for **testing**. This project was created as an experiment to see if the node.js module `child_process` with the export `exec` could power an entire terminal, and to fulfill the need for terminal technologies in the browser.

## Features

- **RHEL-based terminal**: The terminal uses **Amazon Linux**, which is based on **Fedora/CentOS**.
- **Browser-based**: Access a fully interactive Linux terminal directly from your browser.
- **Pre-installed tools**: Essential development tools and utilities are available.
- **API Access**: Programmatically run commands via an API.

## API

WebShell includes an API to execute commands programmatically.

### Endpoint

```http
URL: https://web-terminal-eight.vercel.app/run
Method: POST
Headers: Content-Type: application/json
Body: {"command": "your_linux_command_here"}
```

### Example

To try it, run the following command in your system terminal if `curl` is installed:

```bash
curl -X POST https://web-terminal-eight.vercel.app/run -H "Content-Type: application/json" -d '{"command": "ls -l"}'
```

## Screenshots

### Terminal View

![Screenshot 2024-07-31 8 46 05 AM](https://github.com/user-attachments/assets/1934c424-561d-4063-a1bc-19f468f849fa)


### API View
![Screenshot 2024-07-28 11 49 40 AM](https://github.com/user-attachments/assets/a4a4ecd2-7b37-4744-891d-b5aa6c6a136e)

## Customization Commands

WebShell has a variety of commands that allow you to customize your shell to however you want.

- `setfontsize` - Allows you to change the size of the text using `px` or `em`.
- `setfont` - Allows you to change the font of the terminal by providing a font URL in `otf` or `ttf`.
- `setcolor` - Allows you to change the background color by providing a hex code.
- `setbgcolor` - Allows you to change the background color by providing a hex code.
- `setprompt` - Allows you to change the prompt of the terminal `admin@webshell:~$` to whatever you want.

The usage example of each command is below:

```bash
setfont https://webshell-omega.vercel.app/assets/fonts/Pixel_NES.ttf
```
```bash
setcolor #ff0000
```
```bash
setbgcolor #000000
```
```bash
setfontsize 16px
```

```bash
setprompt foo@localhost~$
```

## How it Works

WebShell uses AWS with a Node.js runtime deployed on Vercel. The `typeset` command in the terminal can display the environment variables.

WebShell uses the `child_process.exec` export to run commands.


> **NOTE**: WebShell Should not be used for complicated tasks due to its restrictions.

## Updates

WebShell now has node.js support! Just type `node` and then You can run JavaScript.

## Licensing

WebShell is licensed under the CC0-1.0 license.

## Contact

For more information, please contact the creator.
