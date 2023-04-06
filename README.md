## Description
This commandline-tool written in [Python](https://www.python.org/) removes all `"id"` tags of a `.ipynb` file.

## Installation
### Requirements
- Python3
### Step 1
Clone this repo to a desired location running the following code inside a terminal:
```bash
$ git clone https://github.com/NicolaiKuertoes/remove-notebook-ids.git
```

### Step 2
Create a symbolic link of the `remove-notebook-ids` file to `$HOME/.local/bin/` using the following command:

```bash
$ ln -s <PATH/TO/REPO/remove-notebook-ids> ~/.local/bin/remove-notebook-ids
```

### Step 3
Now you have to add `~/.local/bin` to your `$PATH` variable by including the following line in your `~/.bashrc` or `~/.zshrc` file:

```bash
export PATH="$HOME/.local/bin:$PATH"
```

### Step 4
Restart your terminal and you can now use the `remove-notebook-ids` tool inside any directory.

## Usage
Type `remove-notebook-ids -h` for help.

```bash
$ remove-notebook-ids -h
usage: remove-notebook-ids [-h] -i <file> [<file> ...] [-o [<path>]]

This program backs up all input files and removes all id-tags from the input
files.

options:
  -h, --help            show this help message and exit
  -i <file> [<file> ...], --infiles <file> [<file> ...]
                        specify input files
  -o [<path>], --outpath [<path>]
                        write file(s) to <path> instead of the current working
                        directory (original files stay untouched)

Coded by Nicolai Kürtös with ❤️
```

## Example 1
The command below will result in a `backup` folder being created. The new file will replace the original file.
```bash
$ remove-notebook-ids -i assignment_1_foo.ipynb
```

## Example 2
The command below will result in a new directory calles `cleaned`will be created in the current working directory. The processed files will be stored there. The original input files stay untouched &rarr; no `backup` directory will be created.

```bash
$ remove-notebook-ids -i assignment_1_foo.ipynb -o ./cleaned
```

<sub>Coded with ❤️ by Nicolai Kürtös</sub>