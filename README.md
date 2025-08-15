# NeoVim Configuration

A NeoVim configuration forked from [kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim).

## Introduction

While this configuration may work on other operating systems, this setup assumes that you are using Windows and that your terminal application of choice is PowerShell.

This configuration of NeoVim is what works for me personally. Since there are some tools that I regularly use NeoVim with, this setup may also be useful for:

- Those looking to write documents in LaTeX and compile into a PDF;
- Those who write documentation in Markdown; or
- Those developing projects in Deno.

## Installation

You do not need to have any other packages installed to run this setup. Not even NeoVim. The configuration files will do the majority of the setup for you. Follow the steps below, and it should work.

For Windows, you need to clone this repository directly to the `nvim` directory in the local application data directory. You can navigate there using `cd $env:LOCALAPPDATA`. There shouldn't be a `nvim` or `nvim-data` directory there. If you see them, delete them. Next, while in the `LOCALAPPDATA` directory, execute `git clone https:\\github.com\Rustic-Citrus\nvim-config.git nvim`.

### Dependencies

Some of the dependencies for this NeoVim setup are opinionated. That is to say, alternative applications could be used, but are not explicitly mentioned. If you're familiar with the alternatives and you prefer to use another instead of the one listed, then all else being equal, NeoVim should work the same way. 

Some of these dependencies are known dependencies of kickstart.nvim and/or NeoVim. They are restated here to save you having to remember or check back with NeoVim and or kickstart.nvim, and can focus on getting started.

Two configuration files can be found in the `config` directory, which are useful for automating setup. If you execute the command, `winget configure -f config\configuration.winget`, while your working directory is `LOCALAPPDATA\nvim`, some of the basic dependencies will be installed.

Once the first installation step has finished, you can open a fresh pane, change your working directory to `LOCALAPPDATA\nvim` (use `cd $env:LOCALAPPDATA\nvim`), and execute `choco install config\packages.config`. This will install the majority of the remaining apps.

As you execute the above commands, be sure to read the output to the console to check for any errors that might occur during the installation process, as they could impact the success of the following steps.

Finally, you need to install Node.js if you don't have it installed already. I recommend nvm-windows, which you can find the latest release for [here](https://github.com/coreybutler/nvm-windows/releases/latest). Once nvm-windows has been installed, you can use `nvm install latest` to install the latest version of Node. Then, use `nvm use latest` to set the latest version as the default for Node.

Once Node is installed, you need to install the tree-sitter-cli package. For it to be accessible globally, you need to pass the global tag when installing it (`npm i -g tree-sitter-cli`).

Finally, a Nerd Font can be used to make NeoVim a bit snazzier. Choose the font you like the most at [Nerd Fonts](https://www.nerdfonts.com/), download it, install it, and set it as the default font for your profile in PowerShell.

