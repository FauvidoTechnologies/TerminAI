# TerminAI_V2

<p align="center">
  <img src="https://img.shields.io/badge/Code-Python-informational?style=flat&logo=python&color=blue" alt="Python" />
  <img src="https://img.shields.io/badge/Code-Bash-informational?style=flat&logo=gnu-bash&color=lightgrey" alt="Bash" />
  <img src="https://img.shields.io/badge/Code-PowerShell-informational?style=flat&logo=powershell&color=blue" alt="PowerShell" />
</p>

## Winner of the [LLM Agents hackathon](https://rdi.berkeley.edu/llm-agents-hackathon/)!

A python based terminal with AI capabilities. Forget commands, just tell it what it do! Check out the demo video [here](https://www.youtube.com/watch?v=nFkwPLMH3D4)

---

**TerminAI** is a powerful terminal that demonstrates the working of multi-model architectures. With TerminAI users can directly type in plain language what they want and have that be executed. TerminAI exhibits duality, that is, if the user enters a bash command directly, then that is immediately executed without the delays introduced by the models.

# Framework 

This is the fifth draft of TerminAI. This is with history implementation.

![TerminAI](./utils/images/TerminAI_V2_draft_7.png)

# Terminal

This is the terminal

![Terminal](./utils/Terminal_GUI/images/terminal_2.png)

# Installing the terminal 

### Linux

Ensure that git is installed

		sudo apt update && sudo apt install git

Then clone the GitHub repo locally. Now you can start installing the dependencies.

		git clone https://github.com/pUrGe12/TerminAI_V2.git && cd TerminAI_V2


### Windows 

Install git using (if no winget then use the [git_website](https://git-scm.com))

		winget install -e --id Git.Git

Then run the following command to clone the it locally,

		git clone https://github.com/pUrGe12/TerminAI_V2.git && cd TerminAI_V2

### MacOS

Install homebrew (mac’s package manager)

		/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Install git and clone the repo

		brew install git && git --version
		git clone https://github.com/pUrGe12/TerminAI_V2.git && cd TerminAI_V2

## Setup

The setup is easy, you are required to obtain 

- [x]  Gemini API keys from over here.
- [x] Create a database over at supabase and get the URL and KEY (the anon public one).

Then you’re required to copy the SQL query over at [table_creation](./utils/setup/table_creation.sql) and run that in the SQL editor of your database.

For Linux and Mac users, run the [setup.sh](./utils/setup/setup.sh) which will take care of the other things using the command below and enter the data whenever required.

For Windows users, execute the PowerShell script [setup.ps1](./utils/setup/setup.ps1) and enter the data whenever required. 

Note for Windows users, you will need to bypass the execution policy to be able to use TerminAI at all (because Windows doesn’t allow command execution by normal users). Use the below command as an administrator in the PowerShell.l

		Set-ExecutionPolicy -Bypass -Scope Process

## Requirements and dependencies

This project uses `uv` for dependency management. Install `uv` if you haven't already:

### Install uv

#### Linux/Mac:
		curl -LsSf https://astral.sh/uv/install.sh | sh

#### Windows (PowerShell):
		powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

Then, install the dependencies:

		uv sync

This will create a virtual environment in `.venv`. To activate it manually:

#### Linux/Mac:
		source .venv/bin/activate

#### Windows (PowerShell):
		.\.venv\Scripts\Activate

## Run

To run the terminal,

		python3 src/main.py

you may need to export wayland to get a better UI, do that using

		export QT_QPA_PLATFORM=wayland

---

## Collaborators
- Achintya Jai (ch23b002@smail.iitm.ac.in)
- Aadi Srivastava (cs23b100@smail.iitm.ac.in)

## Potential things to do

- [ ] Make a better setup file something that tells much more info about the system! For e.g. what the battery name is, model might think BAT0, but you may have BAT1. We gotta think of a clever way to represent this information.

- [ ] Add multimodal support for better integration of textual and visual prompts.

# Things we have to add

---
Priorities

- [ ] We'll have to handle `git` and `cd` separately from others. 

---

- [ ] Introduce verbose outputs for installing things.

---
