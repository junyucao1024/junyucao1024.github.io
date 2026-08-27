---
title: Quick start for the math AI agent "Rethlas"
taxon: Note
---

0. **Set up Rethlas.** If you are using macOS or Linux, follow Shurui Liu's [guide to Rethlas](https://web.stanford.edu/~srliu/homepage/blog/rethlas-guide/). Or, if you have experience working with GitHub projects directly, just clone [the Rethlas repository](https://github.com/frenzymath/Rethlas) and read the README file inside.

If you are using Windows, I would suggest installing `wsl` (Windows Subsystem for Linux) and running Rethlas inside that system. Here are the steps.

1. **Install WSL.** Search for Windows PowerShell, right-click it, and open it with administrator privileges. Then type 

    ```bash
    wsl --install
    ``` 

    (and press `Enter` to run the command; do the same for any later commands you want to run). This installs WSL 2 by default. You may need to restart your computer after the installation. (Personally, I didn’t need to restart my machine—it worked without a reboot.) See [Microsoft's WSL installation guide](https://learn.microsoft.com/en-us/windows/wsl/install) for details.

2. **Open WSL.** After the installation and basic setup of the Linux subsystem (setting up a username/password, for example), type `wsl` in an ordinary PowerShell window to start a terminal inside the Linux subsystem. Alternatively, in Windows Terminal, open the drop-down menu next to the `+` button in the tab bar, then select your Linux distribution to start a WSL terminal.

3. **Set up Rethlas and Codex.** In the WSL terminal, follow Step 0 above. The most important part is to install `codex` inside WSL. Note that this `codex` installation is different from the one under your Windows system, if you have ever installed it there. To install `codex`, type:

   ```bash
   curl -fsSL https://chatgpt.com/codex/install.sh | sh
   ```

   See the [official Codex CLI guide](https://learn.chatgpt.com/docs/codex/cli#getting-started) for details.

   Once Codex is installed, type `codex` and follow the prompts to sign in. You can then give it instructions inside WSL using __natural language__, even if you are not familiar with the command line.

   **Remark.** WSL installs Ubuntu by default, so ask Codex to adapt any macOS or Arch Linux commands in the linked guide to Ubuntu. The Rethlas runner also gives Codex broad permissions inside WSL, so use it only in an environment you trust.

4. **Optional but highly recommended: install Visual Studio Code.** Download and install Visual Studio Code on Windows from its [official website](https://code.visualstudio.com/). Also install the [WSL extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl). Then, from the Rethlas folder in your WSL terminal, type `code .` to open the project.

Further reading:

If you want to know more, I would suggest two follow-up posts by Shurui Liu, one of the Rethlas developers: [a guide to basic terminal use](https://web.stanford.edu/~srliu/homepage/blog/terminal-guide/) and [an advanced guide to Rethlas](https://web.stanford.edu/~srliu/homepage/blog/rethlas-detail/).

To learn more about the command line, I would personally suggest the short MIT course [The Missing Semester of Your CS Education](https://missing.csail.mit.edu/).
