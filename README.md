# 修复 SSH 环境对 terminal、process-explorer 等非文件资源查文件大小，导致报错占用 extension host 的处理资源的问题

```bash
ENOPRO: No file system provider found for resource 'vscode-terminal:/...'
Unable to resolve filesystem provider with relative file path 'process-explorer:default'
```

```powershell
npm i -D @vscode/vsce
# 或者全局： npm i -g @vscode/vsce

Remove-Item -Recurse -Force node_modules
Remove-Item -Force package-lock.json
npm install
npx vsce package
```

# Filesize Hover Explorer

See file sizes instantly by hovering over files in VS Code's Explorer. No more right-clicking or checking properties - just hover and know.

## Features

- Displays human-readable file sizes (B, KB, MB, GB) directly in the VS Code's File Explorer
- Works automatically - no configuration needed
- Super lightweight — no dependencies, just 50 lines of code

![Filesize Hover Explorer in Action](./images/showcase.gif)

## Installation

### Marketplace

Go to the extension [homepage](https://marketplace.visualstudio.com/items?itemName=cyberBabushkin.filesize-hover-explorer) and install the extension. Alternatively, in VS Code, open the Command Palette (`Ctrl+Shift+P` or `Cmd+Shift+P`), type `Install Extensions` and hit Enter. In the search field, type `Filesize Hover Explorer`. Install the extension.

### Manual Installation

Download the latest `.vsix` from the [Releases page](https://github.com/cyberBabushkin/vscode-filesize-hover-explorer/releases). In VS Code, open the Command Palette (`Ctrl+Shift+P` or `Cmd+Shift+P`), type `Install from VSIX`, and select the downloaded file.

Or build it yourself:

```shell
npm install -g @vscode/vsce
git clone https://github.com/cyberBabushkin/vscode-filesize-hover-explorer
cd vscode-filesize-hover-explorer
npm ci
vsce package
```

It will generate the VSIX file in the source directory. The installation is the same as above.

## Known Issues

No known issues! Yet. But you can be the first! Report any issue on Github or create a pull request for changes.

## Support

⭐ Star | 🐛 Report Issues | EVM: `cyberbabushkin.eth`
