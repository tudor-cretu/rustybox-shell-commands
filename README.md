[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/iYoQzOhX)
# Rustybox
This **README** provides an overview of a set of custom shell commands implemented in **Rust**. These commands emulate some of the common functionality found in a Unix-like command-line shell.

## Introduction

The provided Rust code contains a set of custom shell commands that can be run in a terminal. These commands aim to mimic the behavior of common Unix commands, such as **pwd, ls, cat, mkdir, mv, ln, cp, rmdir, rm, touch, chmod, and grep**. The implementation includes both simple commands and more advanced features, such as file and directory operations, recursive functionality, and regular expression searching.

These custom commands were implemented for educational purposes and may not cover all possible edge cases. Please use them with caution, and ensure that you have backups of your important data when using potentially destructive commands.

## List of Commands

**pwd**

    Displays the path of the current directory.

**ls**

    Lists the contents of a directory.
    Supports options **-a (or --all)** for displaying hidden files and **-R (or --recursive)** for recursive listing.

**cat**

    Displays the contents of a file.

**echo**

    Displays the arguments passed to it.
    Supports the **-n** option to suppress the trailing newline.

**mkdir**

    Creates a directory.

**mv**

    Moves or renames a file or directory.

**ln**

    Creates a hard or symbolic link to a file.

**cp**

    Copies a file or directory.
    Supports the **-r (or -R)** option for recursive copying.

**rmdir**

    Removes a directory.

**rm**

    Removes a file or directory.
    Supports options **-r (or --recursive)** and **-d (or --dir)** for controlling removal behavior.

**touch**

    Creates a file or changes the timestamp of a file.
    Supports options **-a (or --access)** and **-m (or --modification)** for changing access and modification times.

**chmod**

    Changes the permissions of a file or directory.
    Supports both numerical and symbolic permissions.

**grep**

    Searches for lines matching a pattern in a file.
    Uses regular expressions to match patterns.

## Error Codes

Each command in this custom shell returns an error code when an operation fails. These error codes can be used to diagnose issues:

    156: Error creating or modifying a file.
    166: Error copying a file or directory.
    176: Invalid command or invalid file/directory.
    186: Error removing a file or directory.
    196: Error removing a directory.
    206: Error creating a symbolic or hard link.
    216: Error moving or renaming a file or directory.
    226: Error creating a directory.
    236: Error reading a file.
    246: Error changing file or directory permissions.

## Dependencies

This project uses the following external dependencies:

   **regex:** A Rust crate for regular expressions.

You can include these dependencies in your **Cargo.toml** if you plan to modify or extend this code.

## Verify

Run the following commands to test your homework:

You will have to install NodeJS (it is installed in the codespace)

```bash
# Clone tests repository
git submodule update --init 

# Update tests repository to the lastest version
cd tests
git pull 
cd ..

# Install loadash
npm install lodash
```

Install rustybox

```bash
cargo install --path .
```

If the `rustybox` command can't be found, be sure to add the default cargo installation folder into the PATH environment variable

```bash
export PATH=/home/<your username here>/.cargo/bin:$PATH
```

Run tests

```bash
cd tests
# Run all tests 
./run_all.sh

# Run single test
./run_all.sh pwd/pwd.sh
```
