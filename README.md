# wsl-vscode
Personal doc. For installation and basic usage of wsl (Windows subsystem Linux) and vscode on it.

## WSL
### Installation
1. Start `Powershell` or `cmd` in *ADMINISTRATOR* mode, and run:
```
wsl --install
```
This will install wsl for your PC.

2. Go to Microsoft store to search and download `Ubuntu 22.04`. The installation is expected to start automatically.

During installtion, you are required to type in your *username* and *password*. You are *not root* by default, unlike in most docker case.

### Verification
After ubuntu system is installed, you can run it by any of following methods:
- Clicking buttom in the `start` panel.
- Running `wsl` in windows command line or powersehll.

### Recommandations: 
- Write `/home/username/.bashrc`: append `cd /mnt/volume_name/work_space` in the end.
- Change `apt` source: 
```
sudo mv /etc/apt/sources.list /etc/apt/sources.list.bak
sudo vim /etc/apt/sources.list
```
Write in:
```
deb https://mirrors.ustc.edu.cn/ubuntu/ focal main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu/ focal main restricted universe multiverse
deb https://mirrors.ustc.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
deb https://mirrors.ustc.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
deb https://mirrors.ustc.edu.cn/ubuntu/ focal-security main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu/ focal-security main restricted universe multiverse
deb https://mirrors.ustc.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse
```

## VS-Code
### Installation
1. Install VS-Code on windows: download it from https://code.visualstudio.com/Download
2. Install the Remote Development extension pack: search this extension in VS-code on windows.

### Usage
1. Open a WSL terminal window.
2. Navigate to a folder you'd like to open in VS Code
3. Type `code .` in the terminal. First time you run this may take a little extra time for downloading.
4. Enjoy coding~




reference: https://code.visualstudio.com/docs/remote/wsl#:~:text=The%20Visual%20Studio%20Code%20Remote%20-%20WSL%20extension,Linux-based%20applications%20all%20from%20the%20comfort%20of%20Windows.

