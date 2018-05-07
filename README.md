# Kansas City Women in Technology Tools Install

Tools Install is a cross-platform (Windows and MacOS) software installation script to assist Coding & Cocktails attendees install their software automatically. Package managers are used to install applications, [Chocolatey](https://chocolatey.org) for Windows uses and [Homebrew](https://brew.sh/)/[Homebrew Cask](https://caskroom.github.io/) for MacOS.

## Software Installed

### All

* [Google Chrome](https://www.google.com/chrome/)
* [Node.Js](https://nodejs.org/en/)
* [Git](https://git-scm.com/)
* [Atom](https://atom.io/)
* [GitKraken](https://www.gitkraken.com/)

### Windows

* [Chocolatey GUI](https://chocolatey.org/packages/ChocolateyGUI)
* [Cmder](http://cmder.net/)

### MacOS

* [Cakebrew](https://www.cakebrew.com/)

## Installation Steps

### Windows

1. Press <kbd>Windows logo key</kbd>+<kbd>R</kbd> on your keyboard.
    1. Type `powershell.exe`
    2. Press <kbd>Enter</kbd>

2. Copy and Paste the following commands in `PowerShell` and press <kbd>Enter</kbd>:
    
    Note: After pasting the commands below, a User Account Control window may appear mulitple times with a message saying `Do you want to run this application to make changes to your device?` Click <kbd>Yes</kbd>
    
    ```powershell
    Start-Process -FilePath powershell.exe -ArgumentList "Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser -Force; Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" -Verb RunAs

    Start-Process -FilePath powershell.exe -ArgumentList "Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/tnieto88/KCWIT-Tools-Install/rapid-development/src/CaC_ToolsInstall.ps1')" -Verb RunAs

    Set-ExecutionPolicy -ExecutionPolicy AllSigned -Force
    ```

3. The script will download and install the various required applications. It may take some time to complete. Please be patient.

4. If there are any errors or warnings please get a hold of a mentor for help.

5. To view, update, install, or reinstall packages start `Chocolatey GUI` from the `Start` menu.

### MacOS

1. In Spotlight search for `Terminal` and start the application.

2. Copy and Paste the following commands in `Terminal` and press <kbd>Enter</kbd>:
    
    ```shell
    curl -fsSL https://raw.githubusercontent.com/tnieto88/KCWIT-Tools-Install/rapid-development/src/CaC_ToolsInstall.sh | sh
    ```

3. If you are prompted for your password please type it and press <kbd>Enter</kbd> to continue.

4. If there are any errors or warnings please get a hold of a mentor for help.

5. To view, update, install, or reinstall packages start `Cakebrew` from `Applications`.